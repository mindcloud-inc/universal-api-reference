# LinkTwin Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model LinkTwin expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/get-pixel?connectionId=$CONNECTION_ID&limit=25&offset=0&id=493" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## LinkTwin actions that support pagination

- [Get Pixel](actions/get-pixel.md)
- [List Domains](actions/list-domains.md)
- [List Pixels](actions/list-pixels.md)
- [List QR Codes](actions/list-qr-codes.md)
