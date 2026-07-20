# Channex: List Room Types

Retrieves room types from your Channex account.

```
GET https://connect.mindcloud.co/v1/universal/channex/latest/actions/list-room-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channex/latest/actions/list-room-types?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channex/latest/actions/list-room-types?${params}`, {
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
| `propertyId` | string | no | Optional property UUID to narrow the room type list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].attributes.count_of_rooms` | number |  |
| `data[].attributes.default_occupancy` | number |  |
| `data[].attributes.occ_adults` | number |  |
| `data[].attributes.title` | string |  |
| `data[].id` | string |  |
| `data[].relationships.property.data.id` | string |  |
| `data[].type` | string |  |

## Native endpoint

Through the native Channex API, this operation is `GET /room_types` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-room-types.md) for the provider-specific parameters and requirements.

