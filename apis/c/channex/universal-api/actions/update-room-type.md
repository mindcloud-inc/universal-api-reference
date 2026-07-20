# Channex: Update Room Type

Updates a room type in Channex.

```
PUT https://connect.mindcloud.co/v1/universal/channex/latest/actions/update-room-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/channex/latest/actions/update-room-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "roomType": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channex/latest/actions/update-room-type', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "roomType": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | UUID of the room type to update. |
| `roomType` | object | yes | Top-level room_type payload object documented by Channex for room type updates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "count_of_rooms": 1,
          "default_occupancy": 1,
          "occ_adults": 1,
          "title": "string"
        },
        "id": "string",
        "relationships": {
          "property": {
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
| `data.attributes.count_of_rooms` | number |  |
| `data.attributes.default_occupancy` | number |  |
| `data.attributes.occ_adults` | number |  |
| `data.attributes.title` | string |  |
| `data.id` | string |  |
| `data.relationships.property.data.id` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native Channex API, this operation is `PUT /room_types/:id` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-room-type.md) for the provider-specific parameters and requirements.

