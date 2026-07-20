# FDIC Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model FDIC expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fDIC/latest/actions/list-bank-failures?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## FDIC actions that support pagination

- [List Bank Failures](actions/list-bank-failures.md)
- [List Financial Institutions](actions/list-financial-institutions.md)
- [List Historical Aggregate Data](actions/list-historical-aggregate-data.md)
- [List Institution Financials](actions/list-institution-financials.md)
- [List Institution Locations](actions/list-institution-locations.md)
- [List Structure Change Events](actions/list-structure-change-events.md)
- [List Summary Of Deposits](actions/list-summary-of-deposits.md)
