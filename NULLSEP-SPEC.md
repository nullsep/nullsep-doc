# NULLSEP Specification 0.1 - DRAFT PRE-RELEASE

## Abstract

NullSep (NSV) is a file format for storing variable-length tabular (rows and colums) data, similar to tab-limited and comma-separated (CSV) data files.  Nuls (char zero) delimit columns, and newlines delimit rows.

## Datastream structure

### Overview

The structure of an NSV file is
* REQUIRED header row
* Optional header ad metadata rows
* Optional data rows
* Optional trailer rows

### Header row

The header row is a single line of readable text, tightly defined:
* `NSV1` -- First four (4) bytes are the file magic number and file format version
* Optional, whitespace-separate KEY=VALUE options
* `\n` -- Newline terminator
