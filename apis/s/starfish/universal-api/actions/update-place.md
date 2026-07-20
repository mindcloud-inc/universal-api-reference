# Starfish: Update Place

Updates an existing place in a Starfish accommodation.

```
PUT https://connect.mindcloud.co/v1/universal/starfish/latest/actions/update-place
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starfish `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/starfish/latest/actions/update-place" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accommodationId": 1,
  "placeId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/starfish/latest/actions/update-place', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accommodationId": 1,
    "placeId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accommodationId` | number | yes | Accommodation ID. |
| `placeId` | number | yes | Place ID. |
| `latitude` | number | no | Updated place latitude. |
| `longitude` | number | no | Updated place longitude. |

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

Through the native Starfish API, this operation is `PUT /accommodations/:accommodation_id/places/:place_id` (base URL `https://api.camping.care/v21`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-place.md) for the provider-specific parameters and requirements.

