# Recreation.gov Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Recreation.gov expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/list-facility-activities?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Recreation.gov actions that support pagination

- [List Facility Activities](actions/list-facility-activities.md)
- [List Facility Addresses](actions/list-facility-addresses.md)
- [List Public Activities](actions/list-public-activities.md)
- [List Public Assets](actions/list-public-assets.md)
- [List Rec Area Activities](actions/list-rec-area-activities.md)
- [List Rec Area Addresses](actions/list-rec-area-addresses.md)
- [List Rec Area Events](actions/list-rec-area-events.md)
