
class: center, middle

<img src="images/escience.png" width=350>

# IN-VIVO VALIDATION
###of
## Diffusion MRI and tractography
## Ariel Rokem
### The University of Washington eScience Institute

<small>Follow along at: <a href="https://arokem.github.io/2017-05-04-diffusion-stats">https://arokem.github.io/2017-05-04-diffusion-stats</small>

---

layout: true

<div style="position: absolute; left: 650px; top: 370px;">
<image src="images/escience-network.png" width=500px style="opacity:0.4;filter:alpha(opacity=40);"> </div>

---

### White matter: the brain's super-highways

<div style="position: absolute; top: 150px; left: 20px;" >
  <image src="images/optic-radiation-postmortem.png" style="background:none; border:none; box-shadow:none;" height="400">
</div>

---

### Why do we study the white matter?

--

- The biology of cognitive functions

--

- Computational models of brain structure and function

--

- Clinical relevance

---

# Normal behavior is supported by brain connections

<image src="images/OldenDays.png" style="background:none; border:none; box-shadow:none;" height="400">

<small>Image from Catani and ffytche (2015)</small>
---

<image src="images/vanessen.png" style="background:none; border:none; box-shadow:none;" height="600">

<div align="right">
<a href="https://github.com/ericmjonas/vanessen"><small>Felleman & Van Essen, 1991</small></a>
</div>

---

# But these connections are not passive wires

--

Brain connections change with development

--

Individual differences in biology account for variance in behavior

--

The white matter adapts with learning

--

Many neurological and psychiatric disorders affect white matter biology

---

### White matter: the brain's super-highways

<div style="position: absolute; top: 150px; left: 20px;" >
  <image src="images/optic-radiation-postmortem.png" style="background:none; border:none; box-shadow:none;" height="400">
</div>

--

<div style="position: absolute; top: 150px; left: 350px;" >
  <image src="images/nerve-fiber.png" style="background:none; border:none; box-shadow:none;" height="400">
</div>

---

# Isotropic diffusion

<div>
<video width="600" data-setup="{}" autoplay loop>
  <source src="/video/diffusion-isotropic.mp4">
</video>
</div>

---

# Anisotropic diffusion

<video width="600" data-setup="{}" autoplay loop>
  <source src="/video/diffusion-anisotropic.mp4">
</video>

---


# Diffusion MRI

<video preload="auto" width="70%" height="auto" data-setup="{}" autoplay loop ><source src="/video/dMRI-signal-movie.mp4"/></video>

---

layout: false

## Models of the white matter

<div style="position: absolute; left: 500px; top: 650px;" >
  <small>Basser, Mattielo and Le Bihan (1994)</small>
</div>

--

<div style="position: absolute; left: 40px; top: 180px;">
<video width="40%" autoplay loop>
  <source src="/video/tensor-signal-movie.mp4">
</video>
</div>

--

<div style="position: absolute; top: 260px; left: 320px;" >
  <image src="images/q-form.png" style="background:none; border:none; box-shadow:none;" height="70">
</div>

--

<div style="position: absolute; top: 200px; left: 630px;">
<video width="70%" autoplay loop>
<source src="/video/tensor-ellipse-movie.mp4">
</video>
</div>

--

style: middle, center

#### Diffusion Tensor Model

---

# Diffusion indices

--

  <div class="fragment" style="position: absolute; left: 14px;">
  <img src="images/tensor-stats1.png" height="340" style="background:none; border:none; box-shadow:none;" >
  <div style="position: absolute; left: 75px; top: 420px;">
    <small>Mean diffusivity</small>
  </div>

  <div style="position: absolute; left: -8px;">
    <img src="images/md-scale.png" height="40" style="background:none; border:none; box-shadow:none;">
  </div>
  <div style="position: absolute; left: 222px; top:350px; ">
    <img src="images/md-units.png" height="50" style="background:none; border:none; box-shadow:none;">
  </div>
  </div>

--
<div class="fragment fade-in" style="position: absolute; left: 15px;">

  <div style="position: absolute; left: 330px; top:340px">
    <video width="120" autoplay loop>
    <source src="video/diffusion-fa-251.mov">
  </div>

  <div>
  <img src="images/tensor-stats2.png" height="340" style="background:none; border:none; box-shadow:none;" >
  </div>

  <div style="position: absolute; left: 350px; top: 420px;">
    <small>Fractional anisotropy</small>
  </div>

</div>

--

  <div class="fragment fade-in" style="position: absolute; left: 15px;">
  <img src="images/tensor-stats3.png" height="340" style="background:none; border:none; box-shadow:none;" >
  <div style="position: absolute; left: 600px; top: 420px;">
    <small>Principal diffusion direction</small>
  </div>
  <div style="position: absolute; left: 650px; top:345px; ">
    <img src="images/axes.png" height="80" style="background:none; border:none; box-shadow:none;">
  </div>
  </div>
  </section>

---



# From diffusion to tracks

<div style="position: absolute; left: 210px;">
<img src="images/axial_slice.png" height="450">
</div>

--

<div class = "fragment fade-in" style="position: absolute;">
<canvas id="zoom-box" width="1000" height="1000"></canvas>
</div>

---

<div style="position: absolute; left: 10px; top:70px;">
<img src="images/d2t-bkgrnd.png" style="background:none; border:none; box-shadow:none;" height="505", width="766">
</div>

--

<div style="position: absolute; left: 102px; top:20px;">
<img src="images/tensor_ellipsoids.png" style="background:none; border:none; box-shadow:none; opacity:0.4; filter:alpha(opacity=40);">
</div>


--

<div class = "fragment fade-in" style="position: absolute;">
<canvas id="fiber" width="1000" height="1000"></canvas>
</div>

---



layout: center, middle

# Which model should we use?

---

## Model selection with cross-validation


<div style="position: absolute; left: 500px; top: 650px;" >
  <a href="http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0123272"><small>Rokem et al. (2015)</a></small>
</div>

<image src="images/rokem2015-fig6.png" height="25%">

---

layout: true

---

<div style="position: absolute; top: 10px; left: 20px;" >
  <image src="images/arokem.png" style="background:none; border:none; box-shadow:none;" height="600">
</div>

---

# Neuroimaging in Python

--

<div style="position: absolute; left: 100px; top: 130px;">
<a href="http://dipy.org"><image src="images/dipy-logo.png"  height="8%"></a>
</div>

--

<div style="position: absolute; top: 250px; left: 20px;" >
  <image src="images/dipy_example_xval.png" style="background:none; border:none; box-shadow:none;" height="400">
</div>

---

<div style="position: absolute; top: 10px; left: 20px;" >
  <image src="images/arokem.png" style="background:none; border:none; box-shadow:none;" height="600">
</div>

---

### Cloud computing enables reproducibility

<image src="images/AWS.png" height="25%">

<image src="images/spark-logo-trademark.png" height="200px">


[K-fold cross-validation on 900 brains](https://github.com/arokem/dki-accuracy-reliability)

---

### Stay in touch!

<div style="position:absolute; left: 220px; top:100px;">
  <img src="images/globe-xxl.png" width="100px;" style="background:none; border:none; box-shadow:none;">
  <div style="position:absolute; left: 120px; top:40px;">http://arokem.org
  </div>
</div>
<div style="position:absolute; left: 220px; top:220px;">
  <img src="images/email-11-xxl.png" width="100px;" style="background:none; border:none; box-shadow:none;">
  <div style="position:absolute; left: 120px; top:40px;">arokem@gmail.com
  </div>
</div>
<div style="position:absolute; left: 220px; top:340px;">
  <img src="images/twitter-xxl.png" width="100px;" style="background:none; border:none; box-shadow:none;">
  <div style="position:absolute; left: 120px; top:40px;">@arokem
  </div>
</div>
<div style="position:absolute; left: 220px; top:460px;">
  <img src="images/github-6-xxl.png" width="100px;" style="background:none; border:none; box-shadow:none;">
  <div style="position:absolute; left: 120px; top:40px;">github.com/arokem
  </div>
</div>
