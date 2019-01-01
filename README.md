# Selena is a bot to suggest similar topics in KNIME forum

This repository contains 2 KNIME workflows and 1 CSV file.

"KNIME forum.knwf" is the workflow to create the initial dataset. (You may change the number of loops. The number of current available pages are 0 to 267 = 268 loops)

"Forum reply.knwf" is the workflow which publishes the topic suggestions and updates the initial dataset. (You have to configure the "Send Keys" - nodes 206 & 205 and add your username and password to login to the KNIME forum)

"forum.csv" is the initial dataset which is created by "KNIME forum.knwf" workflow and is used (and gets updated) in "Forum reply.knwf" workflow.

Many Thanks to KNIME team for the KNIME Server and Philipp Katz for the Selenium nodes and also @Aswin for the Java code.

-------------------------------

### Last changes:

Major improvements were applied to make the workflows clearer, faster and optimized. (Considering recommendations from Philipp Katz - Thank you Philipp!)
