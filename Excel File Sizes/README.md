# A few things about file size in Excel  

<img align="right" width="256" height="256" src="./ExcelShrink.png">

1. Formulas usually take up more space than the values you see on screen.  
  a. What's actually stored in the file are the formulas, not the values.  
  
2. You can replace the formulas with the values (copy, paste-special values), but as analysts, we want to "show our work".  
  a. If you do replace a large column of formulas, it's usually a good idea to keep a copy of the formulas handy, perhaps in separate documentation, or even within the same file.  
  
3. Excel actually has several file formats, and some of these have extended functionality:  
  a. XLSX is the default.  It's actually a ZIP file containing folders and XML files that have the data, functions, formatting, etc.  
  b. XLSM is like XLSX, but supports macros.  
  c. XLSB is a "binary" format.  It's usually smaller than XLSX or XLSM.  
	i. There are benefits to using XLSX or XLSM over using XLSB.  
	
	
In this folder, I have three versions of a file.  The original (01...xlsx) has a bunch of formulas.  In the second (02...xlsx), I replaced the formulas with the calculated values (copy, paste-special values), but kept a copy of the formulas at the top.  The third version (02...xls__b__) is the same as the second except I saved it in XLSB format.


_Sample compression ratios_
| File                                         | File Format | Uncompressed Size (MB)| Compressed Size (MB)| Compressed / Uncompressed Ratio|
|----------------------------------------------|:-------------:|---------------------------:|-------------------------:|---------------------------------:|
| 01 -   Smaller Excel - Version with __Formulas__| XLSX | 26.6| 22.4| 0.84|
| 02 -   Smaller Excel - Version with __Values__| XLSX | 18.8| 17.2| 0.91|
| 02b -   Smaller Excel - Version with Values| __XLSB__ | 9.0| 7.5| 0.83|


In this example, by saving values rather than formulas (note we kept the formulas at the top of the sheet in version "02") and saving the file in the XLSB format, we went from ~26MB to ~7MB (after also zipping the binary down).  


