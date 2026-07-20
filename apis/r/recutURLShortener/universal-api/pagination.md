# Recut URL Shortener Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Recut URL Shortener expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/list-branded-domains?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Recut URL Shortener actions that support pagination

- [List Branded Domains](actions/list-branded-domains.md)
- [List Campaigns](actions/list-campaigns.md)
- [List Channel Items](actions/list-channel-items.md)
- [List Channels](actions/list-channels.md)
- [List CTA Overlays](actions/list-cta-overlays.md)
- [List Custom Splash](actions/list-custom-splash.md)
- [List Files](actions/list-files.md)
- [List Links](actions/list-links.md)
- [List Pixels](actions/list-pixels.md)
- [List QR Codes](actions/list-qr-codes.md)
