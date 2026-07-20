# Torque: Get Aave Markets



```
GET https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-aave-markets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Torque `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-aave-markets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-aave-markets?${params}`, {
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
| `chainId` | number | no | Blockchain chain ID. Defaults to Ethereum mainnet when Torque provides a default. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "protocols": [
        {}
      ],
      "strategies": [
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
| `protocols` | array<object> |  |
| `strategies` | array<object> |  |

## Native endpoint

Through the native Torque API, this operation is `GET /enso/aave-markets` (base URL `https://app.torque.fi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-aave-markets.md) for the provider-specific parameters and requirements.

