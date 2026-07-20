# Teachlr Organizations: Filter And Export Transactions



```
GET https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/filter-and-export-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teachlr Organizations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/filter-and-export-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/filter-and-export-transactions?${params}`, {
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
| `currency` | string | no | Filter transactions by currency. |
| `dateFrom` | string | no | Filter transactions created on or after this date. |
| `dateTo` | string | no | Filter transactions created on or before this date. |
| `format` | string | no | Optional export format. |
| `itemType` | string | no | Filter transactions by item type. |
| `search` | string | no | Search text for transactions. |
| `sort` | string | no | Transaction field to sort by. Default: `created_at`. |
| `status` | string | no | Filter transactions by status. |
| `ord` | string | no | Sort direction. Default: `desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "createdAt": "string",
      "currency": "string",
      "id": 1,
      "itemType": "string",
      "status": "string",
      "userEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `id` | number |  |
| `itemType` | string |  |
| `status` | string |  |
| `userEmail` | string |  |

## Native endpoint

Through the native Teachlr Organizations API, this operation is `GET /transactions` (base URL `https://api.teachlr.com/mindcloudteachlr337933/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/filter-and-export-transactions.md) for the provider-specific parameters and requirements.

