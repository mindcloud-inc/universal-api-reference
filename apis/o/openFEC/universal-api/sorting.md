# OpenFEC Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format OpenFEC expects, and each action page lists the fields available to sort.

## OpenFEC actions that support sorting

- [Get Election Summary](actions/get-election-summary.md)
- [List Calendar Dates](actions/list-calendar-dates.md)
- [List Candidate Filings](actions/list-candidate-filings.md)
- [List Candidate History](actions/list-candidate-history.md)
- [List Candidate Totals](actions/list-candidate-totals.md)
- [List Candidates](actions/list-candidates.md)
- [List Committee History](actions/list-committee-history.md)
- [List Committee Reports](actions/list-committee-reports.md)
- [List Committee Totals](actions/list-committee-totals.md)
- [List Committees](actions/list-committees.md)
- [List Disbursements](actions/list-disbursements.md)
- [List Disbursements By Recipient](actions/list-disbursements-by-recipient.md)
- [List Filings](actions/list-filings.md)
- [List Independent Expenditures](actions/list-independent-expenditures.md)
- [List Itemized Receipts](actions/list-itemized-receipts.md)
- [List Receipts By Employer](actions/list-receipts-by-employer.md)
- [List Receipts By Occupation](actions/list-receipts-by-occupation.md)
- [List Receipts By State](actions/list-receipts-by-state.md)
- [List Reports By Entity Type](actions/list-reports-by-entity-type.md)
- [Search Candidates](actions/search-candidates.md)
- [Search Elections](actions/search-elections.md)
- [Search Legal Documents](actions/search-legal-documents.md)
