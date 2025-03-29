---
layout: resume
title: Broadness
---
# Miscoding of occupations in U.S. Surveys


<section class="content-section">
<h3>Miscoding-correction of occupational flows</h3>

<p>In U.S. surveys, occupational codes are frequently miscoded. In many circumstances, this leads to spurious flows: 
workers are coded to change occupations whereas in reality, no transition occured. In 
<i>Confused about Careers</i>, we use design changes in the PSID and CPS to estimate these miscoding probabilities 
and show how these can be used to correct occupational flows. 
</p>

<h4>Data</h4>

<a href="https://sdaro.s3.eu-central-1.amazonaws.com/public/occupation_distance/miscoding.zip">This zip file</a> contains
miscoding probabilities for slightly modified version of the occ1990 standard. The contents are

<ul>
<li><i>_rename_occ.do</i>: aggregates several minor occupation codes </li>
<li><i>_prog_aggregate_2d.do</i>: aggregates occupation codes to two digits</li>
<li><i>_prog_aggregate_1d.do</i>: aggregates occupation codes to single digit</li>
<li><i>gamma_xx.dta</i>: the Gamma matrix containing the miscoding probabilities, at one digit (xx=1d), two digits (xx=2d),
or three digits (xx=3d).</li>
</ul>


</section>




