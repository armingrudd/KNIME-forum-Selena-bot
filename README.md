# Selena bot to suggest similar topics in KNIME forum

This repository contains 2 KNIME workflows and 1 CSV file.

"KNIME forum.knwf" is the workflow to create the initial dataset.

"Forum reply.knwf" is the workflow which publishes the topic suggestions and updates the initial dataset. (You have to configure the "Send Keys" - nodes 6 & 8 and add your username and password to login to the KNIME forum)

"forum.csv" is the initial dataset which is created by "KNIME forum.knwf" workflow and is used in "Forum reply.knwf" workflow.

Many Thanks to KNIME team for the KNIME Server and Philipp Katz for the Selenium nodes and also @Aswin for the Java code.

-------------------------------

### Last changes:

#### "Forum reply.knwf":

File Reader: Replaced with a new one for the new CSV file.

Table Creator - node 200 (General terms): New general terms added.

JSON Path - node 41: New path added. (Now gets topic key as well)

Rule-based Row filter - node 134: Now match on topic keys instead of URLs. (This was changed because a user may change the topic title that makes both new and previous links valid, So if a topic title with one post is edited, the workflow wouldn't suggest the old URL now)

Column Expressions - node 197: All the expressions are now simplified.

New "Constant Value coulmn" added to include topic key.

"GroupBy" nodes are edited to include topic key.

##### Older updates for this workflow:

Cell Splitters - nodes 108 & 117 (Converting terms from string to collection): From list to set (Now they keep unique terms)

Rule-based Row filter and Row filter - node 134 & 138 (filtering on matching terms to term count ratio): The threshold of the ratio for each of "term" and "term q" columns was changed to 0.3 and total ratio threshold was changed to 0.75

Table Creator - node 200 (General terms): New general terms added

Column Expressions - node 197: New special characters added to be replaced

#### "KNIME forum.knwf":

Table Creator - node 200 (General terms): New general terms added.

JSON Path - node 41: New path added. (Now gets topic key as well)

Column Expressions - node 197: All the expressions are now simplified.

"GroupBy" nodes are edited to include topic key.

##### Older updates for this workflow:

Table Creator - node 200 (General terms): New general terms added

Column Expressions - node 197: New special characters added to be replaced

#### "Forum reply.knwf":

Now has new column named "draft key"
