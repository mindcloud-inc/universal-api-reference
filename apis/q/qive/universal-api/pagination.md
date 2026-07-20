# Qive Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Qive expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qive/latest/actions/list-authorized-ctes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Qive actions that support pagination

- [List Authorized CTes](actions/list-authorized-ctes.md)
- [List Authorized NFes](actions/list-authorized-nfes.md)
- [List CTe Events](actions/list-cte-events.md)
- [List CTe Events V2](actions/list-cte-events-v2.md)
- [List CTe-OS Events](actions/list-cte-os-events.md)
- [List Emitted NFes](actions/list-emitted-nfes.md)
- [List Emitted NFSes](actions/list-emitted-nfses.md)
- [List NFe Events V2](actions/list-nfe-events-v2.md)
- [List NFe Manifests](actions/list-nfe-manifests.md)
- [List NFe Manifests V2](actions/list-nfe-manifests-v2.md)
- [List NFSe Events](actions/list-nfse-events.md)
- [List Not-Taker CTe-OS](actions/list-not-taker-cte-os.md)
- [List Not-Taker CTes](actions/list-not-taker-ctes.md)
- [List Received NFes](actions/list-received-nfes.md)
- [List Received NFSes](actions/list-received-nfses.md)
- [List Received NFSes V2](actions/list-received-nfses-v2.md)
- [List Taker CTe-OS](actions/list-taker-cte-os.md)
- [List Taker CTes](actions/list-taker-ctes.md)
- [List Transporter NFes](actions/list-transporter-nfes.md)
