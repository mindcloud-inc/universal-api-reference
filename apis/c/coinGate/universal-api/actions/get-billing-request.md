# CoinGate: Get Billing Request

Retrieves a billing request from CoinGate by ID.

```
GET https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-billing-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinGate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-billing-request?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/get-billing-request?${params}`, {
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
| `id` | string | yes | CoinGate billing request ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dueDays": 1,
      "id": 1,
      "status": "string",
      "title": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dueDays` | number |  |
| `id` | number |  |
| `status` | string |  |
| `title` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native CoinGate API, this operation is `GET /billing/requests/:id` (base URL `https://api.coingate.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-billing-request.md) for the provider-specific parameters and requirements.

