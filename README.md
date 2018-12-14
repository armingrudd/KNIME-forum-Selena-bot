# KNIME forum auto reply

This repository contains 2 KNIME workflows and 1 CSV file.

"KNIME forum.knwf" is the workflow to create the initial dataset.

"Forum reply.knwf" is the workflow which publishes the topic suggestions and updates the initial dataset.

"forum.csv" is the initial dataset which is created by "KNIME forum.knwf" workflow and is used in "Forum reply.knwf" workflow.

Many Thanks to KNIME team for the KNIME Server and Philipp Katz for the Selenium nodes and also @Aswin for the Java code.

-------------------------------

Last changes to the workflows:

"Forum reply.knwf":

Cell Splitters - node 108 & 117 (converting terms from string to collection): From list to set (Now keeps unique terms)

Rule-based Row filter and Row filter - node 134 & 138 (filtering on matching terms to term count ratio): The threshold of the ratio for each of "term" and "term q" columns was changed to 0.3 and total ratio threshold was changed to 0.75

Table Creator - node 200 (general terms): New general terms added

Column Expressions - node 197: New special characters added to be replaced

"KNIME forum.knwf":

Table Creator - node 200 (general terms): New general terms added

Column Expressions - node 197: New special characters added to be replaced
