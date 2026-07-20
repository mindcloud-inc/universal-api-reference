# OpenFEC Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format OpenFEC expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## OpenFEC actions that support filtering

- [Get Election Summary](actions/get-election-summary.md)
- [List Calendar Dates](actions/list-calendar-dates.md)
- [List Candidate Filings](actions/list-candidate-filings.md)
- [List Candidate Totals](actions/list-candidate-totals.md)
- [List Candidates](actions/list-candidates.md)
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
