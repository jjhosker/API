# Client Project:  Country Analysis by GDP and Income Group for 2012
# Introduction
### This repository creates a report that examines data from the World Bank in 2012 by country on Gross Domestic Product (GDP) combined with country specific Federal Statistics.   

# Running R Code
### 1. To run this R-code, download the following files to your directory below.  
####     - RMakefile_CaseStudy1.R
####     - GatherData_CaseStudy1.R
####     - PlotFunctions_CaseStudy1.R
####     - CaseStudy1PDF.Rmd
####     - R version:  SessionInfo.txt (for reference of libraries and R-version)
### 2. The output files are also included in the repository can be downloaded and are provide as reference for the client.
####     - Raw:      FEDSTATS_Country.csv
####     - Raw:      GDP_Country.csv
####     - Cleaned:  GDPFEDclean.csv
####     - PDF Report:  CaseStudy1PDF.pfd
####     - R version:  SessionInfo.txt (for reference of libraries and R-version)
### 3.  Execute RMakefile_CaseStudy1.R in R studio to run all the R code. RMakefile_CaseStudy1.R to loads all the libraries, read the raw data, create the cleaned data and perform the analysis for this client study.  The csv files will be created in the same directory as the project that you created on your computer.  In addition, we save the R session information that provided the version of R and all the library and packages being utilized.  
####     - The RMakefile_CaseStudy.R executes the makefile GatherData_CaseStudy1.R, which installs the packages and load the libraries.  A message indicating that the libraries loaded may appear after executing the R code.  If a failure occurs please check both the function "packagelibrary.check" in the makefile GatherData_CaseStudy1.R and SessionInfo.txt file in the GitHub directory referenced above.
### 4.  Execute CaseStudy1PDF.Rmd to generate the PDF file in this repository (installation of MikTex is required as detailed in point 6 in the Repository Description below).

# Repository Description
### Below is a listing of all the files in this repository: [\textcolor{blue}{https://github.com/jjhosker/CaseStudy1}](https://github.com/jjhosker/CaseStudy1).  It contains the following important files:

###   1.  README:  This file provides information in detail of each of the files in the GitHub repository and instructions on how to run the R code for this analysis. 
  
###   2.  RMakefile_CaseStudy1.R:  This is the main R makefile that takes the cleaned data and performs all the analysis required for this project and in this report. In cleaning the data, we read in the csv files and in some cases re-name variables and reset data types.  In addition, we remove NAs and blanks in the data.  Finally, we merge the data by the unique country code in both datasets and create and output one cleaned and merged dataset (GDPFEDclean).
  
###   3. GatherData_CaseStudy1.R:  This R makefile is called by RMakefile_CaseStudy1.R above.  First this R makefile provides commands to install all required R-libraries (commented out) and then loads the R-libraries.  Second, this R makefile downloads in the csv data files from  World Bank websites using URLs, reads the downloaded csv files, creates the raw data, and creates the cleaned data sets.   This makefile then saves the cleaned data set as a csv file.  In addition, this R makefile merges the GDP with the Federal Statistical data set into one data set.  Finally, this makefile saves the sessionInfo for the R version, libraries and packages used to a file called SessionInfo.txt.

###   4. PlotFunctions_CaseStudy1.R:  This R Makefile loads plot functions to plot Figures 1 and 2 used in RMakefile_CaseStudy1.R and CaseStudy1PDF.Rmd.

###   5.There are three data files created below:  two downloaded raw datsets downloaded from the World Bank URLs and one cleaned data set.   In addition, we provide a text file (SessionsInfo.txt) containing all the R session information including the current R version and all the libraries and packages being utilized. 
####     - Raw:  FEDSTATS_Country.csv
####     - Raw:  GDP_Country.csv
####     - Cleaned:  GDPFEDclean.csv
####     - R version:  SessionInfo.txt

###  6.  Finally the CaseStudy1PDF.Rmd file runs the main RMakefile_CaseStudy1.R and extracts code to generates this "CaseStudy1PDF.pdf"" report.   This report uses code that that is extracted from the main RMakefile_CaseStudy1.R and then run.
###      - To use this Rmd file to create a PDF, the user has to install MikTex (the non-basic version).  The URL with instructions to install MikTex is [\textcolor{blue}{MikText Install website}](https://miktex.org/howto/install-miktex).
