# TrueLayer: Legacy Submit Embedded Payment Step

Submits a legacy embedded payment step in TrueLayer.

```
PUT https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/legacy-submit-embedded-payment-step
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/legacy-submit-embedded-payment-step" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trueLayer/latest/actions/legacy-submit-embedded-payment-step', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | TrueLayer legacy payment initiation request ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorization_flow": {},
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorization_flow` | object |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TrueLayer API, this operation is `POST /v2/single-immediate-payment-initiation-requests/:id/authorization-flow/actions` (base URL `https://api.truelayer-sandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/legacy-submit-embedded-payment-step.md) for the provider-specific parameters and requirements.

