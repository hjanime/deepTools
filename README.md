======================================================================
deepTools: user-friendly tools for the normalization and visualization of deep-sequencing data.
======================================================================

deepTools address the challenge of visualizing the large amounts of data 
that are now routinely generated from sequencing centers in a meaningful
way. To do so, deepTools contain useful routines to process the mapped
reads data through removal of duplicates and different filtering options
to create coverage files in standard bedGraph and bigWig file formats.
deepTools allow the creation of normalized coverage files or the
comparison between two files (for example, treatment and control).
Finally, using such normalized and standardized files, multiple
visualizations can be created to identify enrichments with
functional annotations of the genome. For a gallery of images that
can be produced and a description of the tools see
http://f1000.com/posters/browse/summary/1094053

![example heatmap](https://raw.github.com/fidelram/deepTools/master/examples/heatmaps.png)
===================
Install from source
===================

The easiest way to install deepTools is by downloading the
source file and using python pip or easy_install tools:

	$ pip install deepTools
	$ vim [deepTools folder]/config/deepTools.cfg

The `deepTools.cfg` file contains several variables that
need to be adjusted.
 
Other option is to clone the repository
	
	$ git clone https://github.com/fidelram/deepTools

Then go to the deepTools directory, edit the `deepTools.cfg` 
file and then run the install script a:

	$ cd deepTools
	$ vim config/deepTools.cfg
	$ python setup.py install
	

By default, the script will install python library and executable
codes globally, which means you need to be root or administrator of
the machine to complete the installation. If you need to
provide a nonstandard install prefix, or any other nonstandard
options, you can provide many command line options to the install
script.

	$ python setup.py --help

To install under a specific location use:

	$ python setup.py install --prefix <target directory>


Galaxy Installation with the Tool Shed
======================================

deepTools can be easily integrated into [Galaxy](http://galaxyproject.org). All wrappers and dependencies are 
available in the [Galaxy Tool Shed](http://testtoolshed.g2.bx.psu.edu/view/bgruening/deeptools).


Installation via Galaxy API (recommended)
-----------------------------------------
   
At first generate an [API Key](http://wiki.galaxyproject.org/Admin/API#Generate_the_Admin_Account_API_Key) for your admin 
user and run the the installation script:

	python ./scripts/api/install_tool_shed_repositories.py --api YOUR_API_KEY -l http://localhost:8080 --url http://testtoolshed.g2.bx.psu.edu/ -o bgruening -r c8a0dc481493 --name deeptools --tool-deps --repository-deps --panel-section-name deepTools

The -r argument specifies the version of deepTools. You can get the latest revsion number from the test tool shed or with the following command:

	hg identify http://testtoolshed.g2.bx.psu.edu/repos/bgruening/deeptools

You can watch the installation status under: Top Panel → Admin → Manage installed tool shed repositories

Installation via webbrowser
---------------------------

- go to the [admin page](http://localhost:8080/admin)
- select *Search and browse tool sheds*
- Galaxy test tool shed → Sequence Analysis → deeptools
- install deeptools


For support, questions, or feature requests contact: deeptools@googlegroups.com 
