# Scope: Module 2.4

## What it does
Creates level-2/summary-table.md containing one Markdown table that
compares my NOI worksheet with Claude's response in
level-1/1.3 Grounded Intelligence - Rent Roll AI Check (1).pdf.
The table has three columns: Figure, My worksheet, Claude's response.
It has six rows: effective rental income, other income, effective gross
income, operating expenses, in-place NOI, and going-in cap rate.

## What it does not do
- Does not change any file in level-1/.
- Does not correct, recalculate, or round any figure. It copies the
  numbers exactly as they appear in the PDF.
- Does not add rows, commentary, or a "who was right" column.

## How I will know it works
1. Row count: the table has exactly 6 data rows.
2. Values: every cell matches these figures, written before the build:
   - Effective rental income: $169,800 / $171,300
   - Other income: $6,600 / $6,600
   - Effective gross income: $224,700 / $177,900
   - Operating expenses: $79,800 / $79,800
   - In-place NOI: $144,900 / $98,100
   - Going-in cap rate: 8.28% / 5.61%
3. No side effects: after the build, git status shows no changes
   inside level-1/.
4. Renders: on GitHub, summary-table.md displays as a table, not as
   raw | characters.