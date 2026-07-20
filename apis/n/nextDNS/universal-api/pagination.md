# NextDNS Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model NextDNS expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/get-analytics-destinations-by-country?connectionId=$CONNECTION_ID&limit=25&offset=0&profileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## NextDNS actions that support pagination

- [Get Analytics Destinations by Country](actions/get-analytics-destinations-by-country.md)
- [Get Analytics Devices](actions/get-analytics-devices.md)
- [Get Analytics DNSSEC](actions/get-analytics-dnssec.md)
- [Get Analytics Domains](actions/get-analytics-domains.md)
- [Get Analytics Encryption](actions/get-analytics-encryption.md)
- [Get Analytics IP Versions](actions/get-analytics-ip-versions.md)
- [Get Analytics IPs](actions/get-analytics-ips.md)
- [Get Analytics Protocols](actions/get-analytics-protocols.md)
- [Get Analytics Query Types](actions/get-analytics-query-types.md)
- [Get Analytics Reasons](actions/get-analytics-reasons.md)
- [Get Analytics Status](actions/get-analytics-status.md)
- [Get Logs](actions/get-logs.md)
