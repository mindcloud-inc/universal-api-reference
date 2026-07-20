# Starfish: Create Place

Creates a new place in a Starfish accommodation.

```
POST https://connect.mindcloud.co/v1/universal/starfish/latest/actions/create-place
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starfish `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/starfish/latest/actions/create-place" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accommodationId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/starfish/latest/actions/create-place', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accommodationId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accommodationId` | number | yes | Parent accommodation ID. |
| `name` | string | no | Optional place name. |

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

Through the native Starfish API, this operation is `POST /accommodations/:accommodation_id/places` (base URL `https://api.camping.care/v21`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-place.md) for the provider-specific parameters and requirements.

