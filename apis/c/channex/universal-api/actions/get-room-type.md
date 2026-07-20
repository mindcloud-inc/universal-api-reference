# Channex: Get Room Type

Retrieves a room type from Channex.

```
GET https://connect.mindcloud.co/v1/universal/channex/latest/actions/get-room-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channex/latest/actions/get-room-type?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channex/latest/actions/get-room-type?${params}`, {
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
| `id` | string | yes | UUID of the room type to retrieve. |

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

Through the native Channex API, this operation is `GET /room_types/:id` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-room-type.md) for the provider-specific parameters and requirements.

