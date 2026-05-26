---
title-slide: false
bibliography: references.bib
csl: vancouver.csl
citeproc: true
theme: serif
background-color: "#ffffff"
transition: slide
navigationMode: linear
hash: true
---

:::: {.columns}
::: {.column width="50%"}

## Sample slides
#### PlaceHolderName
#### Universiti Malaysia Perlis
#### [placeholder@email.com](mailto:placeholder@email.com)

<audio id="bg-music" src="media/audio/sb.m4a" loop></audio>

<div id="audio-credit"
     style="position: absolute; bottom: 40px; right: 20px; font-size: 0.6em; opacity: 0.6;">
  Music: “Adrift” by Scott Buckley (CC BY 4.0)
</div>

<script>
  document.addEventListener('DOMContentLoaded', () => {
    const audio = document.getElementById('bg-music');
    const credit = document.getElementById('audio-credit');

    // hide credit by default
    credit.style.display = 'none';

    const test = new Audio('media/audio/bgm.mp3');

    test.addEventListener('canplaythrough', () => {
      // bgm.mp3 exists → use it, keep credit hidden
      audio.src = 'media/audio/bgm.mp3';
    }, { once: true });

    test.addEventListener('error', () => {
      // bgm.mp3 missing → sb.m4a will play → show credit
      credit.style.display = 'block';
    }, { once: true });

    document.addEventListener('click', () => {
      if (Reveal.getIndices().h === 0) {
        audio.volume = 0.5;
        audio.play();
      }
    }, { once: true });

    Reveal.on('slidechanged', (event) => {
      if (event.indexh > 0) { audio.pause(); }
      else { audio.play(); }
    });
  });
</script>

:::

::: {.column width="50%"}
![](media/pics/logo1.png)
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Slide one
**Key Concepts:**
- Energy conservation per @carnot1824.
- $\Delta U = Q - W$
:::

::: {.column width="50%"}
![](media/pics/sample.png)
:::
::::

---

<span class="slide-title" data-title="My Hidden Slide Name"></span>

![](media/pics/wide.jpeg)

---

:::: {.columns}
::: {.column width="50%"}
### The Master Equation
The fundamental relation of thermodynamics:

$$\Delta U = Q - W$$

The work done $W$ is positive when the system expands against an external pressure.
:::

::: {.column width="50%"}
<video data-src="media/videos/sample.mp4" data-autoplay loop muted width="100%"></video>
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Visualizing the Gas Law
**Interactive Model:**

- P, V, and T relationships.
- Use the slider to adjust pressure.
- Observe the phase boundary.
:::

::: {.column width="50%"}
<iframe 
  data-src="media/plots/sample.html" 
  width="100%" 
  height="500px" 
  style="border:none;" 
  scrolling="no">
</iframe>
:::
::::

---

## Age Distribution

::::{.columns}
:::{.column width='40%'}
### Demographics
This histogram shows the spread of ages within the bigclass dataset, highlighting the most common age groups.
:::

:::{.column width='60%'}
<iframe data-src='media/plots/hist_age.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

## Math Performance by Sex

::::{.columns}
:::{.column width='40%'}
### Academics
A comparison of average Math scores between male and female students.
:::

:::{.column width='60%'}
<iframe data-src='media/plots/bar_math.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

## Weight Analysis

::::{.columns}
:::{.column width='40%'}
### Physical Metrics
Boxplot showing the distribution, median, and variance of weight across different genders.
:::

:::{.column width='60%'}
<iframe data-src='media/plots/box_weight.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

## Height vs Weight

::::{.columns}
:::{.column width='40%'}
### Correlation
Exploring the relationship between height and weight, categorized by sex.
:::

:::{.column width='60%'}
<iframe data-src='media/plots/scatter_hw.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

## Quality Control Chart

::::{.columns}
:::{.column width='40%'}
### Process Stability
Individual control chart (X-bar One) for Machine 1 at 303K and 100 Pressure.
:::

:::{.column width='60%'}
<iframe data-src='media/plots/control_chart.html' width='100%' height='500px' style='border:none;'></iframe>
:::
::::

---

## Key Statistics

### Machine 1 Summary
Filtered at Temp: 303, Pressure: 100


- **Mean:** 51.0460
- **Median:** 51.0911
- **Std Dev:** 0.5839



---
# Bibliography
<div id="refs"></div>
