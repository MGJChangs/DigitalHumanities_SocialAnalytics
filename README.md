# DigitalHumanities_SocialAnalytics
School Project

1) Provenance

The Repertorium of Police Ordinances of the Early Modern Period dataset provides an overview of the laws and regulations of Bern between 1528 and 1798. It is based on the twelve volumes of the Repertorium of Policey Ordinances of the Early Modern Period, edited by Karl Härter and Michael Stolleis. The dataset (policey-bern_DHIntro.csv) contains 4,087,577 bytes, with 178 columns and 4932 rows. The relevant variables for this research include Date, Form, Scope, Matters, Archive and Title. They contain information on the timeline of the created laws (e.g. number of laws over the years), their types, as well as their themes.

2) Data model

The data is stored in a flat file, where each row corresponds to a legislation that was being passed or edited. For specific variables such as matters, it follows a hierarchical database model where multiple child nodes (specific categories) are grouped under one parent node (generic category).

3) Curation of the data and steps took to enrich the data

First, the removal of columns that have null values (empty) in all the rows. For instance, the columns TerOrg, TerOrgID and TerDistrict. Additionally, columns where every row has duplicate values were dropped, as they did not provide new  information. Examples of this are the columns LegislatorID, LegislatorName, LegislatorTitle, TerID, TerLabel etc. The dataset is largely consistent, however, some  values containing special characters needed to be cleaned further - this was done using Python Pandas encoding (utf-8). 
 
Second, the original text in the dataset needed to be translated from German to English for the analysis. We translated the dataset with a file polmat.ttl, which contained a systematic taxonomy in excess of 1.800 matters regulated by police ordinances (last revised: Oct 2021). It is a SKOS vocabulary encoded in ttl/"turtle" format by Annemieke Romein and Andreas Wagner (Rhonda-Org., n.d.).

4) Tools used: Python, Pandas and Tableau


