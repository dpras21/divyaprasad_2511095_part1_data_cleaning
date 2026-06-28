# Cleaning Log

## 1. List of Issues Found

- Missing values found in `region`.
- Missing values found in `ship_mode`.
- Missing values found in `discount`.
- Exact duplicate records were identified.
- Duplicate order IDs with conflicting information were identified.
- Negative discount values were found.
- Discount values greater than the allowed range were found.
- Ship dates earlier than order dates were found.

## 2. Cleaning Actions Performed

- Removed exact duplicate records from the dataset.
- Filled missing `region` values with "Unknown".
- Filled missing `ship_mode` values with "Unknown".
- Replaced missing discount values with `0` where other sales fields were valid.
- Flagged negative discount values as "Invalid Discount".
- Flagged discount values above the allowed range as invalid.
- Flagged records where ship date was earlier than order date.
- Created calculated columns such as profit margin, order month, and order year.

## 3. Business Rules Applied

- Missing `region` values were filled with "Unknown" and flagged in the quality report.
- Missing `ship_mode` values were filled with "Unknown" and flagged in the quality report.
- Missing discount values were treated as `0` only when other sales fields were valid.
- Negative discount values were flagged as invalid.
- Discount values above the allowed range were flagged as invalid.
- Cancelled orders were excluded from completed sales summaries.
- Failed payment orders were excluded from completed sales summaries.
- Refunded orders were summarized separately.
- Records with ship dates earlier than order dates were flagged as invalid shipping records.

## 4. Assumptions Made

- Missing region values were assumed to belong to an unknown region.
- Missing ship mode values were assumed to be unknown.
- Missing discounts were assumed to be `0` only when other required sales fields were available.
- Flagged records were retained for reporting purposes instead of being deleted.

## 5. Records Removed

- Exact duplicate records were removed from the dataset.

## 6. Records Flagged

- Records with negative discounts were flagged.
- Records with discount values above the allowed range were flagged.
- Records with ship dates earlier than order dates were flagged.
- Duplicate records with conflicting information were flagged for manual review.

## 7. Limitations of the Cleaning Process

- Some conflicting duplicate records require manual verification.
- Business assumptions were used for missing values.
- External validation of customer and product information was not performed.




