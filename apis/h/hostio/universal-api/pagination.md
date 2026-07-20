# Host.io Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Host.io expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hostio/latest/actions/list-domains-by-adsense-id?connectionId=$CONNECTION_ID&limit=25&offset=0&value=pub-1556223355139109" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Host.io actions that support pagination

- [List Domains by AdSense ID](actions/list-domains-by-adsense-id.md)
- [List Domains by ASN](actions/list-domains-by-asn.md)
- [List Domains by Backlink Target](actions/list-domains-by-backlink-target.md)
- [List Domains by Email Address](actions/list-domains-by-email-address.md)
- [List Domains by Facebook Handle](actions/list-domains-by-facebook-handle.md)
- [List Domains by Google Analytics ID](actions/list-domains-by-google-analytics-id.md)
- [List Domains by Google Tag Manager ID](actions/list-domains-by-google-tag-manager-id.md)
- [List Domains by Instagram Handle](actions/list-domains-by-instagram-handle.md)
- [List Domains by IP Address](actions/list-domains-by-ip-address.md)
- [List Domains by Mail Server](actions/list-domains-by-mail-server.md)
- [List Domains by Name Server](actions/list-domains-by-name-server.md)
- [List Domains by Redirect Target](actions/list-domains-by-redirect-target.md)
- [List Domains by Twitter Handle](actions/list-domains-by-twitter-handle.md)
