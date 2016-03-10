# dmd2b
DICOM Meta Data DataBase 
#Abstract
This set of python scripts walks down an organized tree of DICOM data and constructs various CSV table files, as well as laying the groundwork for building a database.

# Acknowledgment
This work is a collaboration between the University of Edinburgh Imaging, Scotland (http://www.ed.ac.uk/clinical-sciences/edinburgh-imaging) and the Fetal-Neonatal Neuroimaging Developmental Science Centre, Boston Children’s Hospital (http://www.childrenshospital.org/research-and-innovation/research/centers/fetal-neonatal-neuroimaging-and-developmental-science-center). It was funded by a SINAPSE (http://www.sinapse.ac.uk/) Postdoctoral and Early Career Exchange grant awarded to Samuel Danso who is a staff of the University of Edinburgh to visit Boston which resulted in this work. 




# Prerequisite   
Python 3+ needs to be installed 

# Getting Started
```
Make a directory containing a tree of DICOM files

Make a directory for program files 

Make a directory of output files
```

# Satisfy dependencies

#### Dependencies required:
```
1. Download pydicom from  http://www.pydicom.org/

2. Download dateutil package from https://pypi.python.org/pypi/python-dateutil/
```
Installing from source code
There are several ways to install pydicom and dateutil as subsequently described  but the easiest option is:
```
Unzip downloaded package zipped  files into the programs directory
```

Ubuntu
```
sudo apt-get install pydicom

sudo apt-get install python3-dateutil

```

Mac
```
sudo port install pydicom
sudo port install python3-dateutil
```

#### Check out the repo

```
git clone https://github.com/FNNDSC/dmd2b.git
```

# To run

Edit the following lines in DicomInfoExtract.py  to point to DICOM and output directories

```
os.chdir(/the/path/to/DICOM/)

outputDir = (/the/path/to/output")

```
From the terminal:
```
start python3 Interpreter

>> import DicomInfoExtract.py
```

# Output options
Once run, there are two options available:

#### To display 
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

#### To save files as CSV
Patient details - details of patients or subjects scanned
```
saveToFile(extractPatientDetails(retrieveDicomFiles()),'filename')

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


