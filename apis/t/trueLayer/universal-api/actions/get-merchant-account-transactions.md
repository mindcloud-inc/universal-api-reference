# TrueLayer: Get Merchant Account Transactions

Retrieves merchant account transactions from TrueLayer.

```
GET https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-merchant-account-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-merchant-account-transactions?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/get-merchant-account-transactions?${params}`, {
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
| `id` | string | yes | TrueLayer merchant account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount_in_minor": 1,
      "created_at": "string",
      "currency": "string",
      "id": "string",
      "next_cursor": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount_in_minor` | number |  |
| `created_at` | string |  |
| `currency` | string |  |
| `id` | string |  |
| `next_cursor` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native TrueLayer API, this operation is `GET /v3/merchant-accounts/:id/transactions` (base URL `https://api.truelayer-sandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-merchant-account-transactions.md) for the provider-specific parameters and requirements.

