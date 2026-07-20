# Overledger: List Supported Fungible Tokens



```
GET https://connect.mindcloud.co/v1/universal/overledger/latest/actions/list-supported-fungible-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Overledger `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/overledger/latest/actions/list-supported-fungible-tokens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/overledger/latest/actions/list-supported-fungible-tokens?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `location` | string | no | Optional Overledger location filter, when supported by the endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contractType": "string",
      "decimalPlaces": 1,
      "documentationUrl": "https://example.com",
      "functions": [
        {}
      ],
      "location": {},
      "smartContractId": "string",
      "unit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contractType` | string | Token contract standard or type. |
| `decimalPlaces` | number | Number of decimal places supported by the token. |
| `documentationUrl` | string | Overledger documentation URL for the token, when returned. |
| `functions` | array<object> | Supported token functions. |
| `location` | object | Supported blockchain location. |
| `smartContractId` | string | Token smart contract identifier when provided. |
| `unit` | string | Token unit or symbol returned by Overledger. |

## Native endpoint

Through the native Overledger API, this operation is `GET /v2/tokens/fungible` (base URL `https://api.overledger.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-supported-fungible-tokens.md) for the provider-specific parameters and requirements.

