# Rein_JB

## File formats

Information related to one and the same chorale is represented in multiple variants and formats.
Each comes with its own advantages and disadvantages and users should make informed choices.
Filenames function as IDs in this context in the sense that files representing (information from)
the same chorale share the same filename prefix.

### Authoritative file format: MSCX

At the moment, only one file format in this dataset can be trusted to contain the full amount of 
information to the highest degree of accuracy: the uncompressed MuseScore files ending on 
`.mscx` which can be opened with MuseScore 3 or 4.
To date, we allow modification of these files using 
[MuseScore version 3.6.2](https://github.com/musescore/MuseScore/releases/tag/v3.6.2) exclusively.
However, we use the latest version of MuseScore 4 
(v4.4.4 at the time of writing this in February 2025) to convert these files to MEI and musicXML.
Apart from these format, the information from the MuseScore files is accessible by means of 
tabular files in TSV format, 3 per chorale: `*.notes.tsv`, `*.measures.tsv`, and `*.chords.tsv`
(although the naming of the last is misleading as it contains mainly markup, lyrics, bass figures, etc.).

The latest version of the Python library `ms3` is used to batch convert the MuseScore files
to other formats (`ms3 convert`) and to extract score information to TSV files (`ms3 extract`).

### MEI

To date, MuseScore 4 is able to convert files to MEI Basic 5.0 format. Take these files with a 
grain of salt as we cannot guarantee congruence with the source files.
The quality of these files makes them unsuitable for music research but they may serve as a 
starting point for a well-curated scholarly edition.
In the long run, provided the maturing of the relevant tools, the MEI files should take on 
the role of being the authoritative format.
Until then, they should not be manually modified because they are to be re-generated by conversion
and overwritten once the authoritative MuseScore files are modified.

### musicXML

For convenience and in addition, we offer the chorales in musicXML format. However, experience
shows that musicXML files output by MuseScore come with a number of issues and conversion errors.
These files are unsuited for scholarly work but some users may still appreciate their availability.

### TSV files

Tab-separated files are a dialect of CSV files and can be used the exact same way.
The most convenient way of viewing them is through a spreadsheet program such as LibreOffice Calc
(Excel, Numbers, Sheets, etc.) or a text editor with TSV support/plugin.
Power users may want to load them in their favourite programming language or statistical software.

You can look up what any column means in the documentation of ms3: https://ms3.readthedocs.io/columns

The most important TSV file is called `metadata.tsv`. It contains one row per chorale,
and comes with a number of columns that describe the piece in numerous ways.
A synoptic overview of the most important columns can be found 
[here](https://dcmlab.github.io/mozart_piano_sonatas/#how-to-read-metadata-tsv).

## Overview
|        file_name        |measures|labels|
|-------------------------|-------:|-----:|
|A-MCAU_RE1755-001_SID080 |      10|     0|
|A-MCAU_RE1755-002        |      13|     0|
|A-MCAU_RE1755-003        |      13|     0|
|A-MCAU_RE1755-004_SID046 |      16|     0|
|A-MCAU_RE1755-005_SID097 |      14|     0|
|A-MCAU_RE1755-006_SID069 |      15|     0|
|A-MCAU_RE1755-007_SID037 |      13|     0|
|A-MCAU_RE1755-008_SID096 |      23|     0|
|A-MCAU_RE1755-009_SID036 |      10|     0|
|A-MCAU_RE1755-010_SID011 |      14|     0|
|A-MCAU_RE1755-011_SID001 |      11|     0|
|A-MCAU_RE1755-012_SID002 |      13|     0|
|A-MCAU_RE1755-013_SID012 |      18|     0|
|A-MCAU_RE1755-014_SID021 |      16|     0|
|A-MCAU_RE1755-015_SID085 |      13|     0|
|A-MCAU_RE1755-016_SID029 |      14|     0|
|A-MCAU_RE1755-017_SID077 |      15|     0|
|A-MCAU_RE1755-018        |      26|     0|
|A-MCAU_RE1755-019_SID060 |      13|     0|
|A-MCAU_RE1755-020_SID087 |      26|     0|
|A-MCAU_RE1755-021        |      10|     0|
|A-MCAU_RE1755-022_SID039 |      11|     0|
|A-MCAU_RE1755-023_SID046 |      31|     0|
|A-MCAU_RE1755-024_SID088 |      10|     0|
|A-MCAU_RE1755-025        |      17|     0|
|A-MCAU_RE1755-026_SID026 |      13|     0|
|A-MCAU_RE1755-027_SID089 |       9|     0|
|A-MCAU_RE1755-028        |      22|     0|
|A-MCAU_RE1755-029_SID042 |      13|     0|
|A-MCAU_RE1755-030        |      12|     0|
|A-MCAU_RE1755-031_SID017 |      15|     0|
|A-MCAU_RE1755-032_SID091 |      12|     0|
|A-MCAU_RE1755-033_SID025 |      13|     0|
|A-MCAU_RE1755-034        |      10|     0|
|A-MCAU_RE1755-035_SID081 |      16|     0|
|A-MCAU_RE1755-036_SID086 |      14|     0|
|A-MCAU_RE1755-037_SID004 |      20|     0|
|A-MCAU_RE1755-038_SID005 |      18|     0|
|A-MCAU_RE1755-039        |       9|     0|
|A-MCAU_RE1755-040_SID003 |      12|     0|
|A-MCAU_RE1755-041_SID028 |      19|     0|
|A-MCAU_RE1755-042_SID066 |      28|     0|
|A-MCAU_RE1755-043_SID023 |      15|     0|
|A-MCAU_RE1755-044_SID072 |      14|     0|
|A-MCAU_RE1755-045        |      33|     0|
|A-MCAU_RE1755-046_SID059 |      13|     0|
|A-MCAU_RE1755-047_SID008 |      14|     0|
|A-MCAU_RE1755-048        |      19|     0|
|A-MCAU_RE1755-049        |      15|     0|
|A-MCAU_RE1755-050        |      11|     0|
|A-MCAU_RE1755-051_SID032 |       9|     0|
|A-MCAU_RE1755-052_SID073 |      19|     0|
|A-MCAU_RE1755-053_SID076 |       7|     0|
|A-MCAU_RE1755-054        |      13|     0|
|A-MCAU_RE1755-055_SID065 |      15|     0|
|A-MCAU_RE1755-056_SID054 |      13|     0|
|A-MCAU_RE1755-057        |      17|     0|
|A-MCAU_RE1755-058_SID006 |      14|     0|
|A-MCAU_RE1755-059_SID007 |      13|     0|
|A-MCAU_RE1755-060        |      18|     0|
|A-MCAU_RE1755-061        |      17|     0|
|A-MCAU_RE1755-062        |      13|     0|
|A-MCAU_RE1755-063_SID024 |      18|     0|
|A-MCAU_RE1755-064_SID068 |      10|     0|
|A-MCAU_RE1755-065        |      11|     0|
|A-MCAU_RE1755-066_SID090 |      10|     0|
|A-MCAU_RE1755-067        |      13|     0|
|A-MCAU_RE1755-068        |      16|     0|
|A-MCAU_RE1755-069_SID014 |      16|     0|
|A-MCAU_RE1755-070_SID009 |      11|     0|
|A-MCAU_RE1755-071_SID010 |      10|     0|
|A-MCAU_RE1755-072_SID013 |       9|     0|
|A-MCAU_RE1755-073        |      13|     0|
|A-MCAU_RE1755-074        |      25|     0|
|A-MCAU_RE1755-075_SID018 |      15|     0|
|A-MCAU_RE1755-076_SID082 |      22|     0|
|A-MCAU_RE1755-077_SID092 |      10|     0|
|A-MCAU_RE1755-078        |      19|     0|
|A-MCAU_RE1755-079        |      14|     0|
|A-MCAU_RE1755-080        |      15|     0|
|A-MCAU_RE1755-081_SID062 |      10|     0|
|A-MCAU_RE1755-082_SID015 |      15|     0|
|A-MCAU_RE1755-083_SID079 |      10|     0|
|A-MCAU_RE1755-084        |       9|     0|
|A-MCAU_RE1755-085_SID093 |      10|     0|
|A-MCAU_RE1755-086_SID016 |      11|     0|
|A-MCAU_RE1755-087_SID033 |      12|     0|
|A-MCAU_RE1755-088        |      24|     0|
|A-MCAU_RE1755-089        |      10|     0|
|A-MCAU_RE1755-090        |      13|     0|
|A-MCAU_RE1755-091        |      16|     0|
|A-MCAU_RE1755-092        |      14|     0|
|A-MCAU_RE1755-093_SID067 |      16|     0|
|A-MCAU_RE1755-094_SID019 |      19|     0|
|A-MCAU_RE1755-095        |      15|     0|
|A-MCAU_RE1755-096_SID078 |      18|     0|
|A-MCAU_RE1755-097_SID020 |      21|     0|
|A-MCAU_RE1755-098        |      14|     0|
|A-MCAU_RE1755-099        |      21|     0|
|A-MCAU_RE1755-100        |      25|     0|
|A-MCAU_RE1755-101        |      14|     0|
|A-MCAU_RE1755-102a_SID022|      10|     0|
|A-MCAU_RE1755-102b_SID070|      13|     0|
|A-MCAU_RE1755-103        |      15|     0|
|A-MCAU_RE1755-104_SID074 |      12|     0|
|A-MCAU_RE1755-105        |      22|     0|
|A-MCAU_RE1755-106_SID027 |      13|     0|
|A-MCAU_RE1755-107_SID055 |       8|     0|
|A-MCAU_RE1755-108        |      15|     0|
|A-MCAU_RE1755-109        |      16|     0|
|A-MCAU_RE1755-110        |      14|     0|
|A-MCAU_RE1755-111_SID043 |      13|     0|
|A-MCAU_RE1755-112        |      13|     0|
|A-MCAU_RE1755-113_SID057 |      36|     0|
|A-MCAU_RE1755-114        |      15|     0|
|A-MCAU_RE1755-115        |      19|     0|
|A-MCAU_RE1755-116        |      22|     0|
|A-MCAU_RE1755-117        |      16|     0|
|A-MCAU_RE1755-118_SID030 |      12|     0|
|A-MCAU_RE1755-119_SID038 |      25|     0|
|A-MCAU_RE1755-120        |      18|     0|
|A-MCAU_RE1755-121        |      16|     0|
|A-MCAU_RE1755-122_SID031 |      29|     0|
|A-MCAU_RE1755-123_SID041 |      16|     0|
|A-MCAU_RE1755-124        |      30|     0|
|A-MCAU_RE1755-125        |      20|     0|
|A-MCAU_RE1755-126_SID058 |      15|     0|
|A-MCAU_RE1755-127        |       9|     0|
|A-MCAU_RE1755-128        |      21|     0|
|A-MCAU_RE1755-129        |      24|     0|
|A-MCAU_RE1755-130_SID047 |      10|     0|
|A-MCAU_RE1755-131_SID095 |      13|     0|
|A-MCAU_RE1755-132_SID094 |      10|     0|
|A-MCAU_RE1755-133_SID034 |      78|     0|
|A-MCAU_RE1755-134_SID035 |      16|     0|
|A-MCAU_RE1755-135        |      10|     0|
|A-MCAU_RE1755-136_SID053 |      13|     0|
|A-MCAU_RE1755-137        |      17|     0|
|A-MCAU_RE1755-138_SID040 |      12|     0|
|A-MCAU_RE1755-139_SID083 |      13|     0|
|A-MCAU_RE1755-140_SID048 |      12|     0|
|A-MCAU_RE1755-141        |      13|     0|
|A-MCAU_RE1755-142        |       9|     0|
|A-MCAU_RE1755-143        |       7|     0|
|A-MCAU_RE1755-144        |      12|     0|
|A-MCAU_RE1755-145        |      13|     0|
|A-MCAU_RE1755-146_SID044 |      11|     0|
|A-MCAU_RE1755-147        |      13|     0|
|A-MCAU_RE1755-148        |      23|     0|
|A-MCAU_RE1755-149        |      14|     0|
|A-MCAU_RE1755-150        |      12|     0|
|A-MCAU_RE1755-151_SID045 |      26|     0|
|A-MCAU_RE1755-152        |      13|     0|
|A-MCAU_RE1755-153        |      38|     0|
|A-MCAU_RE1755-154        |      10|     0|
|A-MCAU_RE1755-155        |       8|     0|
|A-MCAU_RE1755-156        |      18|     0|
|A-MCAU_RE1755-157        |      19|     0|
|A-MCAU_RE1755-158        |       8|     0|
|A-MCAU_RE1755-159        |      15|     0|
|A-MCAU_RE1755-160_SID049 |      22|     0|
|A-MCAU_RE1755-161        |      18|     0|
|A-MCAU_RE1755-162_SID050 |      13|     0|
|A-MCAU_RE1755-163_SID051 |      26|     0|
|A-MCAU_RE1755-164_SID052 |      13|     0|
|A-MCAU_RE1755-165        |      13|     0|
|A-MCAU_RE1755-166_SID056 |      10|     0|
|A-MCAU_RE1755-167_SID075 |      13|     0|
|A-MCAU_RE1755-168        |       8|     0|
|A-MCAU_RE1755-169_SID061 |      14|     0|
|A-MCAU_RE1755-170_SID063 |      11|     0|
|A-MCAU_RE1755-171_SID064 |      20|     0|
|A-MCAU_RE1755-172        |      13|     0|
|A-MCAU_RE1755-173        |      11|     0|
|A-MCAU_RE1755-174        |      12|     0|
|A-MCAU_RE1755-175        |      32|     0|
|A-MCAU_RE1755-176        |       8|     0|
|A-MCAU_RE1755-177        |      17|     0|
|A-MCAU_RE1755-178        |      19|     0|
|A-MCAU_RE1755-179        |      13|     0|
|A-MCAU_RE1755-180        |      14|     0|
|A-MCAU_RE1755-181        |      20|     0|
|A-MCAU_RE1755-182_SID084 |      31|     0|
|A-MCAU_RE1755-183        |      12|     0|
|A-MCAU_RE1755-184        |      16|     0|
|A-MCAU_RE1755-185        |      21|     0|
|A-MCAU_RE1755-186        |       9|     0|
|A-MCAU_RE1755-187        |      13|     0|
|A-MCAU_RE1755-188        |      13|     0|
|A-MCAU_RE1755-189_SID071 |      10|     0|
|A-MCAU_RE1755-190        |       8|     0|
|A-MCAU_RE1755-191        |       9|     0|
|A-MCAU_RE1755-192        |      18|     0|
|A-MCAU_RE1755-193        |      17|     0|
|A-MCAU_RE1755-194        |      16|     0|
|A-MCAU_RE1755-195        |      14|     0|
|A-MCAU_RE1755-196        |       9|     0|
|A-MCAU_RE1755-197        |      57|     0|
|A-MCAU_RE1755-198        |      49|     0|
|A-MCAU_RE1755-199        |       9|     0|
|A-MCAU_RE1755-200        |      12|     0|
|A-MCAU_RE1755-201        |      10|     0|


*Overview table automatically updated using [ms3](https://ms3.readthedocs.io/).*
