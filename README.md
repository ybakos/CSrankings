Computer science rankings (beta)
================================

This ranking of top computer science schools is designed to identify institutions and faculty actively engaged in research across a number of areas of computer science. Unlike US News and World Report's approach, which is <a target="_blank" href="http://www.usnews.com/education/best-graduate-schools/articles/science-schools-methodology">exclusively based on surveys</a>, this ranking is entirely metrics-based. It measures the number of publications by faculty that have appeared at the most selective conferences in each area of computer science.

This approach is intended to be difficult to game, since publishing in such conferences is generally difficult: contrast this with other approaches like citation-based metrics, which have been repeatedly shown to be <a target="_blank" href="http://arxiv.org/abs/1212.0638">easy</a> to <a target="_blank" href="http://evaluation.hypotheses.org/files/2010/12/pdf_IkeAntkareISSI.pdf">manipulate</a>. That said, incorporating citations in some form is a long-term goal. <em>This site is in beta and is a work in progress.</em>

---

This repository contains all code and data used to build the computer science rankings website, hosted here:
http://csrankings.org

### Adding or modifying affiliations

To add or modify a faculty member's affiliation, please modify the
file ```faculty-affiliations.csv``` and issue a pull request. Make
sure that the faculty's name corresponds to their <a href="http://dblp.uni-trier.de/search/">DBLP</a> author entry;
for example, Les Valiant's entry is <a
href="http://dblp.uni-trier.de/pers/hd/v/Valiant:Leslie_G=">```Leslie
G. Valiant , Harvard University```</a>.

### Trying it out at home

Because of GitHub size limits, to run this site, you will want to download the DBLP
data by running ``make update-dblp`` (note that this will consume
upwards of 19GiB of memory). To then rebuild the databases, just run
``make``.

You will also need to install libxml2-utils (or whatever package
includes xmllint on your distro), npm, typescript, and python-lxml at
a minimum via a command line like:

``apt-get install libxml2-utils, npm, python-lxml; npm install -g typescript``

