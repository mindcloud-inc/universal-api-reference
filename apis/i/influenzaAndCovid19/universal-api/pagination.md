# Influenza and Covid-19 Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Influenza and Covid-19 expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influenzaAndCovid19/latest/actions/list-emergency-department-respiratory-daily?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Influenza and Covid-19 actions that support pagination

- [List Emergency Department Respiratory Daily](actions/list-emergency-department-respiratory-daily.md)
- [List Emergency Department Visits by Demographic Category](actions/list-emergency-department-visits-by-demographic-category.md)
- [List Provisional Respiratory Death Percentages](actions/list-provisional-respiratory-death-percentages.md)
- [List Viral Respiratory Test Positivity](actions/list-viral-respiratory-test-positivity.md)
