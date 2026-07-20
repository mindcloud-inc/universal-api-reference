# Torque: Get Top Gaining Tokens



```
GET https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-top-gaining-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Torque `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-top-gaining-tokens?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-top-gaining-tokens?${params}`, {
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
| `address` | string | yes | Wallet address. Torque's live endpoint currently requires address for this route. |
| `chain` | string | no |  |
| `limit` | number | no | Maximum number of records to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "decimals": 1,
      "logo": "string",
      "name": "Ava Chen",
      "possible_spam": true,
      "result": [
        {}
      ],
      "symbol": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `decimals` | number |  |
| `logo` | string |  |
| `name` | string |  |
| `possible_spam` | boolean |  |
| `result` | array<object> |  |
| `symbol` | string |  |

## Native endpoint

Through the native Torque API, this operation is `GET /moralis/token-top-gainers` (base URL `https://app.torque.fi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-top-gaining-tokens.md) for the provider-specific parameters and requirements.

