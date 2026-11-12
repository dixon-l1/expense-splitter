# Expense Splitter

Snap receipts, tap who had what, and get the fewest payments that square everyone up.

## Features

- **Receipt scanning**: take or upload photos; Claude reads the line items, tax, tip, fees and discounts. Several photos of one long receipt can be read together. Totals are checked against the printed total.
- **Item assignment**: tap people on each item. Shared items split evenly, or use uneven shares (e.g. 2:1 on a pitcher). Quantity lines like "2× Gyoza" can be broken into separate items.
- **Fair extras**: tax, tip and fees on each receipt are divided in proportion to what each person ordered on it. Quick 18/20/22% tip buttons.
- **Who paid what**: each receipt has a payer; balances are paid minus share.
- **Fewest payments**: balances are split into the most groups that cancel out on their own (exact subset search for up to 16 people with a balance), and each group settles in size − 1 payments.
- **Show the math**: every person's breakdown, line by line, including which amounts were rounded to the cent.

All money is handled in integer cents. Leftover cents from uneven divisions go to the largest fractional remainders, so every receipt adds up exactly.

## Running it

It's a single self-contained `index.html`. Photo reading uses the Claude artifact runtime (`claude.use("sample")`), so scanning works when the page is opened as a Claude artifact; elsewhere the scan button hides and you can type items in by hand.
