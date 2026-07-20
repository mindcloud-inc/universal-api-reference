# PiAPI/Luma (unofficial) Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model PiAPI/Luma (unofficial) expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/list-piapi-luma-task-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## PiAPI/Luma (unofficial) actions that support pagination

- [List PiAPI Luma Task History](actions/list-piapi-luma-task-history.md)
