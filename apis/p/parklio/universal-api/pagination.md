# Parklio Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Parklio expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parklio/latest/actions/list-devices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Parklio actions that support pagination

- [List Devices](actions/list-devices.md)
- [List Gates](actions/list-gates.md)
- [List Gateways](actions/list-gateways.md)
- [List Groups](actions/list-groups.md)
- [List Key Logs](actions/list-key-logs.md)
- [List Lot Entries](actions/list-lot-entries.md)
- [List Lots](actions/list-lots.md)
- [List Parking Places](actions/list-parking-places.md)
- [List Product Errors](actions/list-product-errors.md)
- [List Products](actions/list-products.md)
- [List QR Codes](actions/list-qr-codes.md)
- [List Tariffs](actions/list-tariffs.md)
- [List Terminals](actions/list-terminals.md)
- [List Weblinks](actions/list-weblinks.md)
- [List Zones](actions/list-zones.md)
