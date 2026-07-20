# Blockscout: Get Transactions

Retrieves blockchain transaction listings from Blockscout.

```
GET https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blockscout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blockscout/latest/actions/get-transactions?${params}`, {
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
| `chain_id` | string | no | Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "next_page_params": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> | Transactions returned by Blockscout. |
| `next_page_params` | object |  |

## Native endpoint

Through the native Blockscout API, this operation is `GET /:chain_id/api/v2/transactions` (base URL `https://api.blockscout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transactions.md) for the provider-specific parameters and requirements.

