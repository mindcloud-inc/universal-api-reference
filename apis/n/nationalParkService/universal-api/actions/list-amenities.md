# National Park Service: List Amenities

Retrieves amenities from National Park Service.

```
GET https://connect.mindcloud.co/v1/universal/nationalParkService/latest/actions/list-amenities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a National Park Service `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalParkService/latest/actions/list-amenities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nationalParkService/latest/actions/list-amenities?${params}`, {
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
| `id` | string | no | Amenity unique ID. |
| `q` | string | no | Search term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "limit": "string",
      "start": "string",
      "total": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `limit` | string |  |
| `start` | string |  |
| `total` | string |  |

## Native endpoint

Through the native National Park Service API, this operation is `GET /amenities` (base URL `https://developer.nps.gov/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-amenities.md) for the provider-specific parameters and requirements.

