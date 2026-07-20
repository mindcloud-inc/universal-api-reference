# Certs 365: Check Balance

Retrieves the MATIC balance from Certs 365.

```
GET https://connect.mindcloud.co/v1/universal/certs365/latest/actions/check-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certs 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/certs365/latest/actions/check-balance?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/certs365/latest/actions/check-balance?${params}`, {
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
| `address` | string | yes | Ethereum address to check the balance for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": "string",
      "code": 1,
      "lastUpdate": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | string |  |
| `code` | number |  |
| `lastUpdate` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Certs 365 API, this operation is `GET /api/check-balance` (base URL `https://api1.certs365.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-balance.md) for the provider-specific parameters and requirements.

