# org-timeline-viewer
Org-timeline-viewer is an interactive timeline visualization generated from Org-mode files.

Visualization is created using Python and external libraries like pandas and plotly. All the commands can be executed inside Org-babel blocks, or as an external script. The end result is an interactive graphic.

# Datasets
In order to generate the timeline, you need to provide a dataset that includes Org-mode timestamps.

Right now, Org-timeline-viewer supports the following options:
- org-timeline-viewer-from-org-table, that takes data from an org-table embedded into the demo file.
- org-timeline-viewer-from-org-batch-agenda-csv, that calls emacs in batch mode to export one of the agenda views to an csv file.

# Status
Org-timeline-viewer-from-org-table works independently and is the faster way to check the visualization created.
Org-timeline-viewer-from-org-batch-agenda-csv generates a new file using emacs in batch mode. A test file, equivalent to the org-table, is provided. This option will create some temporary files and then plot them using pandas. This option is the most flexible one for testing but I have found several problems producing the tmp_agenda.csv reliabily. See issues for additional information.

# Inspiration
I have used org-mode for almost 25 years in intermitent periods. Right now I use it for note taking during my data science courses. Today I read Sacha Chua's emacs news and found one topic of my interest: how to visualize a timeline from org-mode files. Following a conversation with Karl Voit on reddit I decided to give it a try :)
