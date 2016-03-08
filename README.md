# dmd2b
DICOM Meta Data DataBase 

# Abstract
This set of python scripts walks down an organized tree of DICOM data and constructs various CSV table files, as well as laying the groundwork for building a database.

##Prerequisite  
Python 3+ needs to be installed 

## Getting Started

### Make a directory containing a tree of DICOM files

### Make a directory for program files 

### Make a directory of output files

### Satisfy dependencies

Dependencies required:
```
1. Download pydicom from  http://www.pydicom.org/

2. Download dateutil package from https://pypi.python.org/pypi/python-dateutil/
```
#### Installing from source code
There are several ways to install pydicom and dateutil as subsequently described  but the easiest option is:
```
Unzip downloaded package zipped  files into the directory where  'DicomInfoExtract.py' program is located
```

#### Ubuntu
```
sudo apt-get install pydicom

sudo apt-get install python3-dateutil

```

#### Mac
```
sudo port install pydicom
```
### Check out the repo

Check out the repository with

```
git clone https://github.com/FNNDSC/dmd2b.git
```

## To run

Edit the following lines in DicomInfoExtract.py  to point to DICOM and output directories

```
os.chdir(/the/path/to/DICOM/)

outputDir = (/the/path/to/output files")

```
From the terminal type the following:
```
python3

import DicomInfoExtract.py
```

# Output options
Once run, there are two options available:

### To display 
Patient details - details of patients or subjects scanned
```
print (extractPatientDetails(retrieveDicomFiles()))
```
Study details - list of studies 
```
print(extractStudyDetails(retrieveDicomFiles()))
```

Series details
```
print(extractSeriesDetails(retrieveDicomFiles()))
```
Addtional information - e.g Primary slice direction, Protocol name
```
print(extractAddtionalHeaderInfo())
```

### To save files as CSV
Patient details - details of patients or subjects scanned
```
saveToFile(extractPatientDetails(retrieveDicomFiles()),'filename')

```
Study details - list of studies 

```
print(extractStudyDetails(retrieveDicomFiles()))
```
Study details - list of studies 
```
saveToFile(extractStudyDetails(retrieveDicomFiles()),'filename')
```
Series details
```
saveToFile(extractSeriesDetails(retrieveDicomFiles()),'filename')
```
Addtional information - e.g Primary slice direction, Protocol name
```
saveToFile(extractAddtionalHeaderInfo(),'filename')
```


