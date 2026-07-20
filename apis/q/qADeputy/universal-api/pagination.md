# QADeputy Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model QADeputy expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qADeputy/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## QADeputy actions that support pagination

- [List Products](actions/list-products.md)
- [List Test Results](actions/list-test-results.md)
- [List Test Run Test Cases](actions/list-test-run-test-cases.md)
- [List Test Runs](actions/list-test-runs.md)
- [List Test Suite Test Cases](actions/list-test-suite-test-cases.md)
- [List Test Suites](actions/list-test-suites.md)
- [List Users](actions/list-users.md)
