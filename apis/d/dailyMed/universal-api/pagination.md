# DailyMed Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model DailyMed expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dailyMed/latest/actions/list-application-numbers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## DailyMed actions that support pagination

- [List Application Numbers](actions/list-application-numbers.md)
- [List Drug Classes](actions/list-drug-classes.md)
- [List Drug Names](actions/list-drug-names.md)
- [List NDCs](actions/list-ndcs.md)
- [List RxCUIs](actions/list-rxcuis.md)
- [List SPLs](actions/list-spls.md)
- [List UNIIs](actions/list-uniis.md)
