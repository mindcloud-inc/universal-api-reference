# Starfish: Get Place

Retrieves a specific place from a Starfish accommodation.

```
GET https://connect.mindcloud.co/v1/universal/starfish/latest/actions/get-place
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starfish `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starfish/latest/actions/get-place?connectionId=$CONNECTION_ID&accommodationId=1&placeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accommodationId": "1",
  "placeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starfish/latest/actions/get-place?${params}`, {
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
| `placeId` | number | yes | Place ID. |

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

Through the native Starfish API, this operation is `GET /accommodations/:accommodation_id/places/:place_id` (base URL `https://api.camping.care/v21`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-place.md) for the provider-specific parameters and requirements.

