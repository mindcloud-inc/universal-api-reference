# Chargeflow: Create Order

Creates a new dispute order in Chargeflow.

```
POST https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "disputeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "disputeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `disputeId` | string | yes | The Chargeflow dispute ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestId` | string |  |

## Native endpoint

Through the native Chargeflow API, this operation is `POST /{disputeId}/order` (base URL `https://api.chargeflow.io/public/2025-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

