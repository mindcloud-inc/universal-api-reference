# Poof: Check Balance

Retrieves wallet balance details from Poof.

```
GET https://connect.mindcloud.co/v1/universal/poof/latest/actions/check-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poof `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poof/latest/actions/check-balance?connectionId=$CONNECTION_ID&crypto=bitcoin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "crypto": "bitcoin"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poof/latest/actions/check-balance?${params}`, {
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
| `crypto` | string | yes | Crypto asset code. Default: `bitcoin`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": "string",
      "currency": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | string |  |
| `currency` | string |  |

## Native endpoint

Through the native Poof API, this operation is `POST /balance` (base URL `https://www.poof.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-balance.md) for the provider-specific parameters and requirements.

