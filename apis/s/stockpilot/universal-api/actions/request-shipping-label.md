# Stockpilot: Request Shipping Label

Requests a shipping label in Stockpilot.

```
POST https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/request-shipping-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/request-shipping-label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "carrierId": "string",
  "orderPk": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/request-shipping-label', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "carrierId": "string",
    "orderPk": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes |  |
| `carrierId` | string | yes |  |
| `orderPk` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entity_id": "string",
      "order_pk": 1,
      "service": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity_id` | string |  |
| `order_pk` | number |  |
| `service` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Stockpilot API, this operation is `POST /shipping/request-label` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-shipping-label.md) for the provider-specific parameters and requirements.

