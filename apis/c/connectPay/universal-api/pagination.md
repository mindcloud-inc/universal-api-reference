# ConnectPay Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model ConnectPay expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/get-account-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## ConnectPay actions that support pagination

- [Get Account Transactions](actions/get-account-transactions.md)
- [Get BaaS Clients](actions/get-baas-clients.md)
- [Get BaaS Merchant Providers](actions/get-baas-merchant-providers.md)
- [Get BaaS Merchant Recurrence Details](actions/get-baas-merchant-recurrence-details.md)
