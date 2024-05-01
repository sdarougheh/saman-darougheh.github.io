---
layout: resume
title: LCP solver
---

<section class="content-section">

<h3>LCP solver for python</h3>

Optimal stopping time problems can often be rewritten as linear complementarity problems (LCP), which allows efficient solution algorithms 
(see for example the <a href="https://benjaminmoll.com/codes/">Stopping time problems on Ben Moll's code section</a>).

a python interface for pathlib, allowing to solve both linear and mixed complementarity problems. Among other requires gcc and cython to install.


Installation

<ol>
<li><a href="https://sdaro.s3.eu-central-1.amazonaws.com/public/lcp/lcp.zip">Download</a> and extract the lcp folder</li>
<li><a href="https://pages.cs.wisc.edu/~ferris/path.html">Download</a> and extract the pathlib folder into lcp/pathlib</li>
<li><a href="https://sdaro.s3.eu-central-1.amazonaws.com/public/lcp/examples.zip">Download</a> and extract the examples folder, use it to replace lcp/pathlib/examples.</li>
<li>Go into lcp/pathlib/examples/SimpleLCP, and run "make -f makefile.lnx" (or other file if not on linux)</li>
<li>Go into lcp/pathlib/examples/Standalone_C, and run "make -f makefile.lnx" (or other file if not on linux)</li>
<li>Go into lcp/, run "python setup.py build_ext --inplace".</li> 
</ol>



</section>