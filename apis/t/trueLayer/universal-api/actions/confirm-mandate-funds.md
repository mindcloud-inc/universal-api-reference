# TrueLayer: Confirm Mandate Funds

Confirms mandate funds in TrueLayer.

```
GET https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/confirm-mandate-funds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/confirm-mandate-funds?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/confirm-mandate-funds?${params}`, {
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
| `id` | string | yes | TrueLayer mandate ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "available": true,
      "balance": 1,
      "currency": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | boolean |  |
| `balance` | number |  |
| `currency` | string |  |
| `id` | string |  |

## Native endpoint

Through the native TrueLayer API, this operation is `GET /v3/mandates/:id/funds` (base URL `https://api.truelayer-sandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/confirm-mandate-funds.md) for the provider-specific parameters and requirements.

