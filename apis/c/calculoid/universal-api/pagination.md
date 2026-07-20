# Calculoid Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Calculoid expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/list-calculator-results?connectionId=$CONNECTION_ID&limit=25&offset=0&calculatorId=109359" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Calculoid actions that support pagination

- [List Calculator Results](actions/list-calculator-results.md)
- [List Calculator Templates](actions/list-calculator-templates.md)
- [List Calculators](actions/list-calculators.md)
- [List Submissions](actions/list-submissions.md)
