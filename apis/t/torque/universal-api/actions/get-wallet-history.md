# Torque: Get Wallet History



```
GET https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-wallet-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Torque `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-wallet-history?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-wallet-history?${params}`, {
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
| `address` | string | yes | Wallet address to query. |
| `chain` | string | no |  |
| `limit` | number | no | Maximum number of records to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "limit": 1,
      "page": 1,
      "page_size": 1,
      "result": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | string |  |
| `limit` | number |  |
| `page` | number |  |
| `page_size` | number |  |
| `result` | array<object> |  |

## Native endpoint

Through the native Torque API, this operation is `GET /moralis/wallet-history` (base URL `https://app.torque.fi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wallet-history.md) for the provider-specific parameters and requirements.

