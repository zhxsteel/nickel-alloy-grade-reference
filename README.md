# Nickel Alloy Grade Reference

A small open reference table that matches common nickel alloy trade names to their UNS numbers, alloy family, what each is known for, and the ASTM product specifications usually used for bar and plate.

The data is in [`nickel-alloy-grades.csv`](nickel-alloy-grades.csv). It is plain CSV, so it opens in Excel, Google Sheets, or any script.

## Columns

| Column | Meaning |
|---|---|
| `grade` | Common trade or grade name |
| `uns` | Unified Numbering System designation |
| `family` | Alloy family |
| `main_elements` | Main alloying elements |
| `known_for` | What the grade is typically chosen for |
| `typical_bar_spec` | ASTM specification usually used for bar |
| `typical_plate_spec` | ASTM specification usually used for plate and sheet |

## Quick example (Python)

```python
import csv

with open("nickel-alloy-grades.csv", newline="") as f:
    grades = {row["uns"]: row for row in csv.DictReader(f)}

print(grades["N10276"]["grade"], grades["N10276"]["typical_plate_spec"])
# Hastelloy C-276 ASTM B575
```

## Notes

- This is a starting reference, not a substitute for the current edition of the standard. Check the exact specification, product form and condition before ordering or designing.
- Trade names such as Inconel, Incoloy, Monel and Hastelloy belong to their respective owners. They are used here only to identify the alloys.
- Corrections and additions are welcome through issues or pull requests.

## About

Maintained by [ZHX Steel](https://zhxsteel.com/), a supplier of nickel alloys, titanium and stainless steel in Wuxi, China.

## License

MIT
