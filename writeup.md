## HW 10.5g Two-Layer Model
### Josh Elms
---

Here I modify the `run.py` script to use a two-layer, rather than eady, model. 

### P1
---
*Include one of the frames of the animation for both the Eady and two-layer simulations*

#### Eady
<img src="eady/snapshots/000_000000050000000.png" alt="eady" width="300"> 

#### Two-layer
<img src="two-layer/snapshots/000_000000050000000.png" alt="two-layer" width="300">

### P2
--- 
*Include the stability analysis plots for both the Eady and two-layer simulations*

I ran the two-layer model by commenting out the Eady initializtion from `run.py:L47-49` and uncommenting `run.py:L43-45`. While this sufficed to change the actual model, it did not seem to change the stability analysis found at `run.py:L68-70`. The only inputs to the stability analysis function `linstab` are `k` and `l`, neither of which (in the code) descends from choices made about the model. It seems that `k` and `l` ought to be the most unstable wavenumbers in both runs, but I'm not sure how to relate the expressions for maximum-unsteady wavenumbers from the respective sections of Vallis to the actual `linstab` function from Callies. I'll include the one and only stability analysis I found (shared by both runs) below: 

<img src="linstab.png" alt="linstab" width="500">

### P3
---
*Perform a qualitative comparison of the behavior of the system based off of the animations (what was the same? what was different?)*

The Eady model generally seems to be more diffusive than the two-layer, based on the Eady's softer colors and smaller zones of anomalous vorticity w.r.t surroundings. The two-layer has sharp gradients and long filaments of vorticity that stretch far away from the source, indicating that mixing is not as intense in that model. Both show similar movement patterns, though, and are quite visually similar when not directly compared. 

Finally (and this is perhaps more related to the initialization rather than the system itself), the mean-state (where the model starts) for the Eady simulation was zonally uniform, whereas the two-layer run seemed to consist of random noise. 

### P4
---
*Provide a description of the differences of the system's stability based off of the stability analysis plots.*

Because I only found one instability plot, I can't really answer this one. 

### P5
---
*A comparison of the differences with those you expected based off of your reading of Vallis ch. 6*

The two-layer system exhibiting those long filaments of vorticity stretching out from a source is consistent with the fact that, as Vallis says on p. 288, "there is no low wavenumber cut-off" for that system; large waves can more readily form and propagate. 