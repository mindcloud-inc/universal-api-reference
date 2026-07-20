# Digistore24: List Purchases

Retrieves a list of purchases from Digistore24.

```
GET https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-purchases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digistore24 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-purchases?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/list-purchases?${params}`, {
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
| `from` | string | no | Start of the purchase time range, for example -24h. Default: `-24h`. |
| `to` | string | no | End of the purchase time range, for example now. Default: `now`. |
| `search` | string | no | Search filters |
| `sortBy` | string | no | Purchase field to sort by, such as date or purchase_id. Default: `date`. |
| `sortOrder` | string | no | Sort direction: asc or desc. Default: `asc`. |
| `loadTransactions` | boolean | no | Include transaction details in the response. Default: `false`. |
| `pageNo` | number | no | Page number starting at 1. Default: `1`. |
| `pageSize` | number | no | Number of purchases per page. Default: `1000`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Digistore24 API returns.

## Native endpoint

Through the native Digistore24 API, this operation is `GET /listPurchases` (base URL `https://www.digistore24.com/api/call`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-purchases.md) for the provider-specific parameters and requirements.

