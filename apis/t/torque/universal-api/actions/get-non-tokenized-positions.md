# Torque: Get Non Tokenized Positions



```
GET https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-non-tokenized-positions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Torque `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-non-tokenized-positions?connectionId=$CONNECTION_ID&eoaAddress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eoaAddress": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-non-tokenized-positions?${params}`, {
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
| `eoaAddress` | string | yes | Externally owned account wallet address. Torque's live endpoint currently requires eoaAddress for this route. |
| `chainId` | number | no | Blockchain chain ID. Defaults to Ethereum mainnet when Torque provides a default. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
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
| `data` | array<object> |  |

## Native endpoint

Through the native Torque API, this operation is `GET /enso/positions/nontokenized` (base URL `https://app.torque.fi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-non-tokenized-positions.md) for the provider-specific parameters and requirements.

