# Channex: Update Rate Plan

Updates a rate plan in Channex.

```
PUT https://connect.mindcloud.co/v1/universal/channex/latest/actions/update-rate-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/channex/latest/actions/update-rate-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "ratePlan": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channex/latest/actions/update-rate-plan', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "ratePlan": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | UUID of the rate plan to update. |
| `ratePlan` | object | yes | Top-level rate_plan payload object documented by Channex for rate plan updates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "currency": "string",
          "rate_mode": "string",
          "sell_mode": "string",
          "title": "string"
        },
        "id": "string",
        "relationships": {
          "property": {
            "data": {
              "id": "string"
            }
          },
          "room_type": {
            "data": {
              "id": "string"
            }
          }
        },
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.attributes.currency` | string |  |
| `data.attributes.rate_mode` | string |  |
| `data.attributes.sell_mode` | string |  |
| `data.attributes.title` | string |  |
| `data.id` | string |  |
| `data.relationships.property.data.id` | string |  |
| `data.relationships.room_type.data.id` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native Channex API, this operation is `PUT /rate_plans/:id` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-rate-plan.md) for the provider-specific parameters and requirements.

