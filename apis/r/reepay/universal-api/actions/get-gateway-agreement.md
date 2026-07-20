# Reepay: Get Gateway Agreement

Retrieves a gateway agreement from Reepay.

```
GET https://connect.mindcloud.co/v1/universal/reepay/latest/actions/get-gateway-agreement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reepay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reepay/latest/actions/get-gateway-agreement?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reepay/latest/actions/get-gateway-agreement?${params}`, {
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
| `id` | string | yes | Agreement id from Reepay. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "offline_agreement": {
        "currencies": [
          "string"
        ],
        "handle": "string",
        "instructions": "string",
        "name": "Ava Chen",
        "payment_term_grace_period_in_days": 1,
        "payment_terms_in_days": 1,
        "payment_type": "string",
        "settle_type": "string"
      },
      "state": "string",
      "test": true,
      "type": "string",
      "usage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `id` | string |  |
| `name` | string |  |
| `offline_agreement.currencies[]` | string |  |
| `offline_agreement.handle` | string |  |
| `offline_agreement.instructions` | string |  |
| `offline_agreement.name` | string |  |
| `offline_agreement.payment_term_grace_period_in_days` | number |  |
| `offline_agreement.payment_terms_in_days` | number |  |
| `offline_agreement.payment_type` | string |  |
| `offline_agreement.settle_type` | string |  |
| `state` | string |  |
| `test` | boolean |  |
| `type` | string |  |
| `usage` | string |  |

## Native endpoint

Through the native Reepay API, this operation is `GET /v1/agreement/:id` (base URL `https://api.frisbii.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-gateway-agreement.md) for the provider-specific parameters and requirements.

