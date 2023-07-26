# Atmospheric Re-entry Dynamics

Atmospheric re-entry is a crucial stage in many space missions, as it involves massive structural and thermal loads on the spacecraft. There are two types of atmospheric re-entries:
<ul>
  <li>Lifting: performed by maneuverable vehicles, where lift force can be controlled to follow a specific trajectory (Space Shuttle).</li>
  <li>Ballistic: reentry vehicles, Mercury capsules, etc. </li>
</ul> 

The aim of this project was to reproduce the figures in reference [1]. This was joint work with [Yi Qiang Ji Zhang](https://github.com/yiqiangjizhang) and [Iván Sermanoukian Molina](https://github.com/Ivan-Sermanoukian).

## The code

A MATLAB script was programmed for this project. To compute the trajectory, it solves the flight mechanics equations using a Runge-Kutta 4 method. 

The main file for the project is  ```main.m``` (who would have thought it), while the other files are functions. Code sections:
<ol>
  <li>Constants: universal constants and Earth/Mars atmospheric data</li>
  <li>Previous calculations: compute properties for each atmospheric layer</li>
  <li>Ballistic reentry: solves ballistic reentries for different ballistic coefficients $(\beta = W / (C_D A))$</li>
  <li>Mercury capsule reentry: solves the ballistic reentry of a Mercury capsule</li>
  <li>Lifting reentry: solves a lifting reentry</li>
  <li>Solution: plots the desired results</li>
</ol> 

Upon execution, the script will prompt for planet number (1 - Earth, 2 - Mars). You can define your own planet in section 1 of the code. As for atmospheric data:
<ul>
  <li>Temperature is used to compute pressure and density.</li>
  <li>Temperature is assumed to behave linearly within an atmospheric layer.</li>
  <li>Elevation of atmospheric layers is defined in ```H_layer_Earth```.</li>
  <li>Temperature gradient of each atmospheric layer is defined in ```lambda_layer_Earth```.</li>
  <li>Heat capacity ratio ($\gamma$) is defined in ```gamma_gas_Earth```.</li>
</ul> 


### Lifting reentry



### Ballistic reentry


## Figures

## References

[1] J.C. Adams Jr. Atmospheric Reentry, June 2003. 2011