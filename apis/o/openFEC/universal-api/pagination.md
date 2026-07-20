# OpenFEC Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model OpenFEC expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/get-election-summary?connectionId=$CONNECTION_ID&limit=25&offset=0&cycle=1&office=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## OpenFEC actions that support pagination

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
