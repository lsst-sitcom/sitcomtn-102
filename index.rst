#################################################################
SITCom Performance Analysis Technote Style and Writing Guidelines
#################################################################

Abstract
========

Quick reference for writing SITCOM technotes. Each section in this technote is intended to reflect the actual suggested structure. It is advisable to maintain the main headers homogeneous across technotes, and structure the report in subheaders as needed by the author. In any case, this technote reflects ideas that could be useful in the procedure of creating and writing a technote, and should be taken as guidelines rather than rules.

Technote abstracts should include a short 2-3 sentence explanation of the goal of the technote. Ideally, it should also include a 1-2 sentence summary of the main conclusions.

*Example: We verify that the pointing accuracy of the system is compliant with the requirement of 5 arcsec RMS. We do this by analyzing star tracker data during a soak test mimicking real scheduled observations. Our conclusions are that the pointing performance is compliant with the requirement, except at low (<30 deg.) elevation measurements.* 

*Example: We explore the problems found on 2024-02-01 on the azimuth drives to diagnose the issue. We study what TMA settings lead to the drives going to fault. Currently not correlation of velocity, acceleration, jerk or initial/final positions are found*.

Please refer to the Appendix for resources for starting a technote and styling.


Introduction
============

This is a short reference to provide guidance and support for creating technotes related to SITCOM activities. For details on how to start, configure and edit a technote, see the `Documenteer documentation <https://documenteer.lsst.io/technotes/index.html>`_. This includes adding yourself as author in the author database file, in case you are not there.

The introduction would expand the details and context in which the technote is written, and why its goals are pursued. In the case of a very straightforward measurement, or self-explanatory, it could be merged with the abstract. 

*Example: Vibrations of the TMA structure immediately after a slew can impact the image quality performance, if they prolong into the time in which data is collected. We need to measure the residual vibration of the TMA in various axes, and in identical conditions as in real observations. These tests should be combined with those that measure the jittering of other mechanical and optical systems in the light path for an overall assessment of the 
optical performance. The results in this technote should be regarded as preliminary because the final TMA settings have not been configured.*

Related Tickets
===============

A bulleted list of related SITCOM tickets and their titles, including those issued to  writing the technote itself, those related to relevant code used to produce the results and any other tickets that can help trace the problem. 

The `list of issues <https://rubinobs.atlassian.net/jira/software/c/projects/SITCOM/issues/?filter=allissues>`_ can help identify appropriate links. 

*Example:*

* `SITCOM-798 <https://rubinobs.atlassian.net/browse/SITCOM-798>`_: *M1M3 - settling time after a slew*
* `SITCOM-1172 <https://rubinobs.atlassian.net/browse/SITCOM-1172>`_: *M1M3 - analyze settling times after a slew statistically*
* `OBS-467 <https://rubinobs.atlassian.net/browse/OBS-467>`_: *Vibrations coming from the top end of TMA*

Related Requirements
====================

(if applicable) A list of the requirements verified by the results of the technote, including code
and title. The full description of the requirement could be added if it facilitates the
interpretation of the results. 

*Example*:

*LTS-88-REQ-0051: The positioning system SHALL be able to meet all its requirements within 3 seconds of ending a short slew (3.5 degrees in 2 seconds)*


Execution Details and Data
==========================

Include scripts (with complete links to Github), data sets used (block number, source of data), and date in which they were executed (this is often helpful). Possibly a short description of procedure and/or how the script was executed, in case it requires a configuration file or specific arguments. The relevant test cases can be highlighted here as well. 

Results
=======

This section can simply show numerical and graphical results, leaving the discussion for another section,  or incorporate also conclusions or take-aways from each of the items as they are presented.

Specific analysis block 1
-------------------------
Use this kind of header and subheaders to organize the results and discussion. For each result block, summarize at the beginning what this section adresses.

Subsubsection for analysis block 1
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Parcel out into subsubsections such as this one if the analysis requires it.

Tables
------
Some recommendations:

* Use bold face to differentiate header column names
* Tables can be included or not in the appropriate sections depending on the importance to complement the text (include) or they are there as reference (put in an appendix).
* Some guidance on making tables on reStructured Text and Sphinx can be found `here <https://sublime-and-sphinx-guide.readthedocs.io/en/latest/tables.html>`_ .

Plots
-----
Some recommendations:

* Make plots as self explanatory as possible, by the use of proper labels, titles, legend, overlaid text.
* Use large fonts for text, label and title, where possible. 
* Always add units to physical quantities.
* Avoid differentiating data ranges with colors. Try to use different line and marker styles. If colors are needed, a recommendation is to upload your plots to `this page <https://www.color-blindness.com/coblis-color-blindness-simulator>`_
* Include error bars
* Highlight requirements or areas in which the viewer has to focus on
* Where applicable provide histogrammed versions of the results and calculate a mean and RMS, or equivalently a Gaussian fit

An example is shown in :numref:`label` :

.. _label:
.. figure:: /_static/azel.png
   :name: fig-azel

   Distribution of slew events, including those that failed the test, in azimuth and elevation, for dayObs 
   20232012.

Discussion
==========
A detailed discussion could have its own section after the Results, but is not always necessary. This is particularly useful when the amount of tables and/or plots require an overall evaluation to be explained in a single section. 

Conclusions
===========
Conclusions should include a clear cut status of the resolution of the goal the technote was designed
to address. In case of requirement verification, this would include PASS/FAIL assessments for each.

If a clear resolution is not found at this time, it is advisable to add a path to said resolution
or further testing, as sometimes technotes are only meant to provide a snapshot of the situation
they are describing. 

This section should not be too long to provide a quick 'single-glance' summary, that together with the abstract, would provide a complete sself contained information piece on the issue at hand.

*Example: Using star tracker data from camera XX on the soak tests performed on observation day XXXX-YY-ZZ we have been able to verify requirement RRR, in mostly all azimuth-elevation combinations. However, in 60% of the cases were pointing was to an elevation below 30 degrees, the offset was beyond the requirement, reaching almost 8 arcseconds.*

Related Documentation
=====================
Documentation references with links to other relevant technotes or Rubin documentation, including other technical bibliography such as papers, conference proceedings, where appropriate.

*Example:*

`LTS-88 <https://docushare.lsst.org/docushare/dsweb/Get/LTS-88/LTS-88.pdf>`_ *M1M3 Mirror Support Design Requirement Document*


Appendix
========

Technote Writing Guide
----------------------

In order to start a technote, as well as some useful tips for using reStructured text, please refer to this `presentation <https://github.com/lsst-sitcom/sitcomtn-102/files/14638694/2020-10-14.Documentation.Ops.Bootcamp.pdf>`_ by the Rubin documentation team. ReStructured text supports LaTeX-style math using the 'math' environment and inverted commas: \:math\:\`x^2+y^2=z^2\` will translate into :math:`x^2+y^2=z^2`.

See `this reference <https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html>`_ for the official reStructured text documentation.

Aditionally, consider using ``monospace`` font for file and directory names.
