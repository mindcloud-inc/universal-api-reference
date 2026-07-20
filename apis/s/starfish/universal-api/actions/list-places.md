# Starfish: List Places

Retrieves places for a specific accommodation in Starfish.

```
GET https://connect.mindcloud.co/v1/universal/starfish/latest/actions/list-places
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starfish `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starfish/latest/actions/list-places?connectionId=$CONNECTION_ID&limit=25&offset=0&accommodationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "accommodationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starfish/latest/actions/list-places?${params}`, {
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
| `accommodationId` | number | yes | Accommodation ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accommodationId": 1,
      "adminId": 1,
      "cleaningStatus": "string",
      "id": 1,
      "meta": {},
      "name": "Ava Chen",
      "placeUid": "string",
      "rank": 1,
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accommodationId` | number |  |
| `adminId` | number |  |
| `cleaningStatus` | string |  |
| `id` | number |  |
| `meta` | object |  |
| `name` | string |  |
| `placeUid` | string |  |
| `rank` | number |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Starfish API, this operation is `GET /accommodations/:accommodation_id/places` (base URL `https://api.camping.care/v21`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-places.md) for the provider-specific parameters and requirements.

