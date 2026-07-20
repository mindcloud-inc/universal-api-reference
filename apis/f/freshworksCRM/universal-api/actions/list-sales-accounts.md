# Freshworks CRM: List Sales Accounts

Retrieves sales accounts from a view in Freshworks CRM.

```
GET https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-sales-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-sales-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-sales-accounts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `viewId` | number | no | Numeric view identifier used for list queries. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "total": 1,
        "total_pages": 1
      },
      "sales_accounts": [
        {
          "avatar": "string",
          "city": "string",
          "country": "string",
          "created_at": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "last_contacted": "2026-05-07T12:00:00.000Z",
          "last_contacted_mode": "string",
          "name": "Ava Chen",
          "open_deals_amount": "string",
          "state": "string",
          "updated_at": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.total` | number | Total count. |
| `meta.total_pages` | number | Total pages. |
| `sales_accounts[].avatar` | string | Avatar URL. |
| `sales_accounts[].city` | string | City. |
| `sales_accounts[].country` | string | Country. |
| `sales_accounts[].created_at` | date | Created timestamp. |
| `sales_accounts[].id` | number | Sales account identifier. |
| `sales_accounts[].last_contacted` | date | Last contacted timestamp. |
| `sales_accounts[].last_contacted_mode` | string | Last contact mode. |
| `sales_accounts[].name` | string | Sales account name. |
| `sales_accounts[].open_deals_amount` | string | Open deals amount. |
| `sales_accounts[].state` | string | State. |
| `sales_accounts[].updated_at` | date | Updated timestamp. |

## Native endpoint

Through the native Freshworks CRM API, this operation is `GET api/sales_accounts/view/:view_id` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sales-accounts.md) for the provider-specific parameters and requirements.

