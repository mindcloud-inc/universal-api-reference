# ReadyCloud Suite: Create Box

Creates a new box in ReadyCloud Suite.

```
POST https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/create-box
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReadyCloud Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/create-box" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderPk": "string",
  "orgPk": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/create-box', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderPk": "string",
    "orgPk": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderPk` | string | yes | ReadyCloud order identifier. |
| `orgPk` | string | yes | ReadyCloud organization identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cod": true,
      "cod_value": "string",
      "confirmation_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_fields": {},
      "declared_value": "string",
      "delivered_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "height": 1,
      "insurance_type": "string",
      "insured_value": "string",
      "items": [
        {}
      ],
      "length": 1,
      "package_type": "string",
      "packaging": {},
      "saturday_delivery": true,
      "ship_cost": "string",
      "shipper_release": true,
      "shipping_docs": [
        {}
      ],
      "tracking": [
        {}
      ],
      "tracking_number": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "weight": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cod` | boolean |  |
| `cod_value` | string |  |
| `confirmation_type` | string |  |
| `created_at` | date |  |
| `custom_fields` | object |  |
| `declared_value` | string |  |
| `delivered_at` | date |  |
| `description` | string |  |
| `height` | number |  |
| `insurance_type` | string |  |
| `insured_value` | string |  |
| `items` | array<object> |  |
| `length` | number |  |
| `package_type` | string |  |
| `packaging` | object |  |
| `saturday_delivery` | boolean |  |
| `ship_cost` | string |  |
| `shipper_release` | boolean |  |
| `shipping_docs` | array<object> |  |
| `tracking` | array<object> |  |
| `tracking_number` | string |  |
| `updated_at` | date |  |
| `url` | string |  |
| `weight` | string |  |
| `width` | number |  |

## Native endpoint

Through the native ReadyCloud Suite API, this operation is `POST /api/v2/orgs/:orgPk/orders/:orderPk/boxes/` (base URL `https://www.readycloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-box.md) for the provider-specific parameters and requirements.

