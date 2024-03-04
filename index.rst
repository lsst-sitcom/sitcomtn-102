################################
Technote Style and Writing Guide
################################

Abstract
========

.. abstract::

   Quick reference for writing SITCOM technotes. Each section in this technote is intended to
reflect the actual suggested structure. It is advisable to maintain the main headers homogeneous
across the technotes for which this is a sensible approach, and structure the report in subheaders
as needed by the author. 

Technote abstracts should include a short 2-3 sentence explanation of the goal of the technote. Ideally, it should also include a 1-2 sentence summary of the main conclusions.

Related Tickets
===============

A bulleted list of related tickets and titles, including those issued to  writing the technote and possibly those related to relevant code used to produce the results.

Related Requirements
====================

(if applicable) A list of the requirements verified by the results of this technote, including code
and title. The full description of the requirement could be added if it facilitates the
interpretation of the results. 

Introduction
============

This is a short reference to provide guidance and support for creating technotes related to SITCOM
activities. For details on how to start, configure and edit a technote, see the `Documenteer documentation <https://documenteer.lsst.io/technotes/index.html>`_. This includes adding yourself as author in the author database file, in case you are not there.

The introduction should expand the details and context in which this technote is written, and why
its goals are pursued. 

Execution Details and Data
==========================

Include scripts (including complete links), data sets, and date in which they were executed (this often helpful). Possibly a short description of procedure and/or how the script was executed, in case it requires a configuration file or specific arguments. 

Results and Discussion
======================

This section can simply show numerical and graphical results, leaving the discussion for another section,  or incorporate also conclusions or take-aways from each of the items as they are presented.

Specific analysis block 1
-------------------------
Use this kind of header and subheaders to organize the results and discussion.


Tables
------


Plots
-----
Some recommendations:

* Make plots as self explanatory as possible, by the use of proper labels, titles, legend, overlaid text.
* Use large fonts for text, label and title, where possible. 
* Always add units to physical quantities
* Avoid differentiating different data ranges with colors. Try to use different line and marker
styles. If colors are needed, a recommendation is to upload your plots to
`this page <https://www.color-blindness.com/coblis-color-blindness-simulator>`_


Conclusions
===========
Conclusions should include a clear cut status of the resolution of the goal the technote was design
to address. In case of requirement verification, this would include PASS/FAIL assessments of each.
If a clear resolution is not found at this time, it is advisable to add a path to said resolution
or further testing, as sometimes technotes are only meant to provide a snapshot of the situation
they are describing. This section should not be too long to provide a quick 'single-glance'
summary, that together with the abstract, would provide a complete set, self contained information
piece on the issue at hand.

Related Documentation
=====================
Documentation references with links to other relevant technotes or Rubin documentation, including other technical bibliography such as papers, conference proceedings, where appropriate.


Appendix
========

Technote Style Guide
--------------------
Text Parts
^^^^^^^^^^
Reasoning:
Using the same structure in all technotes makes it easy to jump in to the needed information

A document should be structured in the following parts

- Introduction
- Main Part
- Summary and Conclusion

Technote Writing Guide
----------------------
Writing tempus
^^^^^^^^^^^^^^
**Suggestion:**

Write in present tense as much as possible.

**Reason:**

This gives the reader a more lively impression.

**Example:**

???


Writing perspective
^^^^^^^^^^^^^^^^^^^
**Suggestion:**

- Passive voice?
- "We" perspective?

**Reason:**

**Example:**

When to update technote
=======================



