# Import-large-spreadsheet-with-million-lines
Group by Skeleton with Position - Large Spreadsheet Data Import
# Group by Skeleton with Position
A memory-efficient solution for large spreadsheet data import

## Author
**Mike Li**  
SAP Labs China, Chengdu  
Email: mike.li01@sap.com

## Abstract
Group by Skeleton with Position is a general solution to import large spreadsheets stably without out-of-memory errors.
It reduces memory usage by nearly 10 times by grouping rows using a lightweight skeleton and position only.
It has been applied in SAP enterprise scenarios for processing millions of rows with 30+ columns.

## Paper
[Group by Skeleton with Position.docx](./Group%20by%20Skeleton%20with%20Position.docx)

## Core Idea
1. Extract a lightweight skeleton (key field) from each row
2. Group rows by skeleton + position (sheet/row/column)
3. Pass compressed stream + positions to sub-procedures
4. Parse data by position to minimize memory cost

## Key Advantages
- No OOM for 1M+ rows × 30+ columns
- Memory usage reduced by 10×–15×
- No manual file splitting
- Supports parallel processing
- Works for SAP / ERP / enterprise data import

## Keywords
data import, large spreadsheet, skeleton, position, memory optimization, SAP, ABAP
