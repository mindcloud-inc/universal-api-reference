# DNSFilter Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model DNSFilter expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/list-all-applications?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## DNSFilter actions that support pagination

- [List All Applications](actions/list-all-applications.md)
- [List All Categories](actions/list-all-categories.md)
- [List All IP Addresses](actions/list-all-ip-addresses.md)
- [List All MAC Addresses](actions/list-all-mac-addresses.md)
- [List All Networks](actions/list-all-networks.md)
- [List All Organizations](actions/list-all-organizations.md)
- [List All Policies](actions/list-all-policies.md)
- [List Application Categories](actions/list-application-categories.md)
- [List Applications](actions/list-applications.md)
- [List Block Pages](actions/list-block-pages.md)
- [List Categories](actions/list-categories.md)
- [List IP Addresses](actions/list-ip-addresses.md)
- [List MAC Addresses](actions/list-mac-addresses.md)
- [List Network Subnets](actions/list-network-subnets.md)
- [List Networks](actions/list-networks.md)
- [List Organizations](actions/list-organizations.md)
- [List Policies](actions/list-policies.md)
