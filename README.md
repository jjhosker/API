# Client Project:  Country Analysis by GDP and Income Group for 2012
# Introduction
### This repository creates a report that examines data from the World Bank in 2012 by country on Gross Domestic Product (GDP) combined with country specific Federal Statistics.   

# Running R Code
### 1. To run this R-code, download the following files to your directory below.  Make sure that you install the packages and/or load the libraries that are detailed in the makefile:  GatherData_CaseStudy1 and SessionInfo.txt (see description below).
####     - RMakefile_CaseStudy1.R
####     - GatherData_CaseStudy1.R
####     - PlotFunctions_CaseStudy1.R
####     - CaseStudy1PDF.Rmd
####     - R version:  SessionInfo.txt (for reference of libraries and R-version)

### 2. The output files are also included in the repository can be downloaded and are below:
####     - Raw:      FEDSTATS_Country.csv
####     - Raw:      GDP_Country.csv
####     - Cleaned:  GDPFEDclean.csv
####     - PDF Report:  CaseStudy1PDF.pfd
### 3.  Execute RMakefile_CaseStudy1.R in R studio to run all the R code.
### 4.  Execute CaseStudy1PDF.Rmd to generate the PDF file in this repository (installation of MikTex is required as detailed above).

# Repository Description
### Below is a listing of all the files in this repository:

###   1.  README:  This file that  provides more information in detail of each of the files in the github directory. 
  
###   2.  RMakefile_CaseStudy1.R:  This is the main R makefile that takes the cleaned data and performs all the analysis required for this project and in this report. In cleaning the data, we read in the csv files and in some cases re-name variables and reset data types.  In addition, we remove NAs and blanks in the data.  Finally, we merges the data by the unique country code in both data sets and create and output one cleaned and merged dataset (GDPFEDclean).
  
###   3. GatherData_CaseStudy1.R:  This R makefile is called by RMakefile_CaseStudy1.R above.  First this R makefile provides commands to install all required R-libraries (commented out) and then loads the R-libraries.  Second, this R makefile downloads in the csv data files from  World Bank websites using URLs, reads the downloaded csv files, creates the raw data, and creates the cleaned data sets.   This makefile then saves the cleaned data set as a csv file.  In addition, this R makefile merges the GDP with the Federal Statistical data set into one data set.  Finally, this makefile saves the sessionInfo for the R version, libraries and packages used to a file called SessionInfo.txt.

###   4. PlotFunctions_CaseStudy1.R:  This R Makefile loads plot functions to plot Figures 1 and 2 used in RMakefile_CaseStudy1.R and CaseStudy1PDF.Rmd.

###   5.There are three data files created below:  two downloaded raw datsets downloaded from the World Bank URLs and one cleaned data set.   In addition, we provide a text file (SessionsInfo.txt) containing all the R session information including the current R version and all the libraries and packages being utilized. 
####     - Raw:  FEDSTATS_Country.csv
####     - Raw:  GDP_Country.csv
####     - Cleaned:  GDPFEDclean.csv
####     - R version:  SessionInfo.txt

####  6.  Finally the CaseStudy1PDF.Rmd file runs the main RMakefile_CaseStudy1.R and extracts code to generates this "CaseStudy1PDF.pdf"" report.   This report uses code that that is extracted from the main RMakefile_CaseStudy1.R and then run.
###      - To use this Rmd file to create a PDF, the user has to install MikTex (the non-basic version).  The URL with instructions to install MikTex is [\textcolor{blue}{MikText Install website}](https://miktex.org/howto/install-miktex).
