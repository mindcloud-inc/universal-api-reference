# UpGuard Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model UpGuard expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/get-portfolio-risk-profile-overview?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## UpGuard actions that support pagination

- [Get Portfolio Risk Profile Overview](actions/get-portfolio-risk-profile-overview.md)
- [List Monitored Vendor Risk Changes](actions/list-monitored-vendor-risk-changes.md)
- [List Monitored Vendors](actions/list-monitored-vendors.md)
- [List Onboarding Requests](actions/list-onboarding-requests.md)
- [List Vendor Domains](actions/list-vendor-domains.md)
- [List Vendor IPs](actions/list-vendor-ips.md)
