# A few things about file size in Excel  

<img align="right" width="256" height="256" src="./ExcelShrink.png">

1. Formulas usually take up more space than the values you see on screen.  
  a. What's actually stored in the file are the formulas, not the values.  
  
2. You can replace the formulas with the values (copy, paste-special values), but as analysts, we want to "show our work".  
  a. If you do replace a large column of formulas, it's usually a good idea to keep a copy of the formulas handy, perhaps in separate documentation, or even within the same file.  
  
3. Excel actually has several file formats, and some of these have extended functionality:  
  a. XLSX is the default.  It's actually a ZIP file containing folders and XML files that have the data, functions, formatting, etc.  
  b. XLSM is like XLSX, but supports macros.  
  c. XLSB is a "binary" format.  It's usually smaller than XLSX or XLSB.  
	i. There are benefits to using XLSX or XLSM over using XLSB.  
	
	
In this folder,  


_Sample compression ratios_
| File                                         | File Format | Uncompressed Size (bytes)| Compressed Size (bytes)| Compressed / Uncompressed Ratio|
|----------------------------------------------|:-------------:|---------------------------:|-------------------------:|---------------------------------:|
| 01 -   Smaller Excel - Version with Formulas| XLSX | 26,561,753| 22,426,663| 0.84|
| 02 -   Smaller Excel - Version with Values| XLSX | 18,825,619| 17,162,996| 0.91|
| 02b -   Smaller Excel - Version with Values| XLSB | 8,998,142| 7,483,636| 0.83|


In this example, by saving values rather than formulas (note we kept the formulas at the top of the sheet in version "02") and saving the file in the XLSB format, we went from ~26MB to ~7MB.  


