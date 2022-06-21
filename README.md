# IDBdash
R dashboard of metrics from the Illinois Data Bank data repository

This R Markdown file produces an html dashboard of various metrics related to the data publications in the Illinois Data Bank. 
Metrics are compiled in 2 csv files: Datasets (which aggregates data on all of the files submitted as part of a dataset), and Datafiles (which looks at individual files).
Download stats are compiled in a JSON file recording each date a dataset was downloaded and the number of downloads on that date. Downloads are currently only explored in one chart showing total downloads per year. In a future version, download stats could be connected with the other datasets for further analysis. The downloads file is stored as txt because I had issues getting the JSON file to load into RStudio correctly.

File Manifest:
IDBdash.Rmd - R code in markdown format that produces the dashboard
IDBdash.html - dashboard exported from R
datasets_2021-12-31.csv - dataset metrics
datafiles_2021-12-31.csv - data file metrics
downloads.txt - JSON download data

Datasets.csv column headings:
doi: DOI that identifies this dataset
pub_date: Date the files in this dataset were first available for download
num_files: Total number of datafiles in this dataset
num_bytes: Combined total size for all files in this dataset, in bytes
total_downloads: Number of downloads for this dataset
num_relationships: Number of related materials, excluding other versions of this dataset
subject: Subject Area of this dataset

Datafiles.csv column headings:
Column Headings
doi: DOI that identifies the dataset this file is part of
pub_date: Date this file was first made available for download
filename: Name of the file, with extension
file_format: Mime type 
num_bytes: Size of this files, in bytes
total_downloads: Number of downloads for this file

Downloads.txt fields:
doi: DOI that identifies this dataset
date: download date
tally: number of downloads on that date

The dashboard could be adapted for use by other repositories provided the metrics files are used as templates. 
Note that the number of subjects should be small. If there are more than 5, the color palettes will need to be expanded. More than 10 probably won't display well.

Created in 2022 by Sandi Caldrone in RStudio 2022.02.3+492 "Prairie Trillium" Release (1db809b8323ba0a87c148d16eb84efe39a8e7785, 2022-05-20) for Windows
Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) QtWebEngine/5.12.8 Chrome/69.0.3497.128 Safari/537.36