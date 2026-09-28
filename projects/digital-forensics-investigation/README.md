# Digital Forensics File Analysis & Evidence Investigation

## Overview

This project documents practical digital forensic analysis completed within an authorised university laboratory environment.

The investigation involved examining unknown files using FTK Imager, identifying their true file formats through hexadecimal file signatures, recording MD5 hashes, recovering the files, and verifying that they could be opened correctly.

Additional forensic analysis was performed using FoldersReport and EnCase to examine directory structures and extract system-level information from supplied forensic evidence.

## Scope

All evidence used in this project was supplied as part of an authorised university digital forensics laboratory environment.

No live, personal, or unauthorised systems were examined.

## Tools Used

- FTK Imager
- EnCase
- EnScript / System Snapshot
- FoldersReport
- Hexadecimal analysis

## Investigation Methodology

The investigation followed a structured forensic process:

1. Load the supplied files into FTK Imager.
2. Examine file properties and record MD5 hashes.
3. Inspect hexadecimal headers and footers.
4. Compare file signatures to known file formats.
5. Determine the correct file extensions.
6. Rename and recover the identified files.
7. Open the recovered files to verify the findings.
8. Analyse extracted directory structures.
9. Examine supplied forensic evidence using EnCase.
10. Document the investigation and preserve screenshot evidence.

# Findings

## Finding 1 – BQ File Identification

The unknown file `BQ` was examined using FTK Imager.

Hexadecimal analysis identified the following file signature:

**Header:** `89 50 4E 47`

**Footer:** `49 45 4E 44 AE 42 60 82`

The signature indicated that the file contained PNG image data.

The MD5 hash recorded during the examination was:

`c85c7755b87705518ecb95e35ae21b0e`

The file was renamed to `BQ.png` and successfully opened, confirming the identified file format.

## Finding 2 – GQ File Identification

The unknown file `GQ` was examined using FTK Imager.

The hexadecimal header was:

`7B 5C 72 74 66 31`

This corresponds to the RTF file signature.

The footer `7D` was identified at the end of the file.

The MD5 hash recorded during the examination was:

`5cac3a4beb5789613341f4a7b259687c`

The file was renamed to `GQ.rtf` and successfully opened as formatted text, confirming the identified file format.

## Finding 3 – LP File Identification

The unknown file `LP` was examined using FTK Imager.

The hexadecimal header was identified as:

`50 4B 03 04`

This indicated that the file was a ZIP archive.

The MD5 hash recorded during the examination was:

`d94772b76754d8a015a588d5e9bf010c`

The file was renamed to `LP.zip` and extracted. The successful extraction confirmed that the file contained compressed internal files.

# Additional Forensic Analysis

## Directory Analysis – FoldersReport

FoldersReport was used to examine the extracted LP directory.

The generated report displayed information including:

- Folder names
- Folder sizes
- Number of files
- Timestamps

The results were sorted by size to assist with identifying larger directories and potential areas of interest.

FoldersReport was useful for preliminary directory analysis, although it was recognised that it does not provide forensic capabilities such as hashing or integrity verification and should therefore be used as a supporting tool rather than as the sole forensic analysis tool.

## EnCase System Analysis

The supplied `BBasher.E01` forensic evidence file was loaded into EnCase.

The System Snapshot EnScript was compiled and executed within EnCase. The resulting output provided system-level information including:

- Operating system information
- Time-zone information
- IP address information
- User information

This demonstrated how forensic tools can be used to extract system context from supplied forensic evidence.

# Skills Demonstrated

- Digital forensic investigation
- FTK Imager
- EnCase
- EnScript
- File hashing
- MD5 analysis
- Hexadecimal analysis
- File signature identification
- File type recovery
- Forensic evidence examination
- Directory analysis
- Evidence documentation

# Evidence

Selected screenshots from the investigation demonstrate the analysis process, including file hashing, hexadecimal examination, file recovery, directory analysis, and EnCase system examination.

# Ethical Considerations

All analysis documented in this project was completed within an authorised university digital forensics laboratory environment using supplied evidence.

# Conclusion

The investigation demonstrated how file signatures, hexadecimal analysis, hashing, and forensic tools can be combined to identify and examine unknown files.

Three unknown files were successfully identified as PNG, RTF, and ZIP formats. Additional analysis using FoldersReport and EnCase demonstrated directory analysis and system-level evidence examination.
