# TravelPerk: Get Trip

Retrieves a trip from TravelPerk.

```
GET https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/get-trip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TravelPerk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/get-trip?connectionId=$CONNECTION_ID&tripId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tripId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/get-trip?${params}`, {
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
| `tripId` | string | yes | The TravelPerk trip identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "booker_id": "string",
      "end": "string",
      "end_datetime_local": "string",
      "end_datetime_utc": "string",
      "end_location": {},
      "id": "string",
      "modified": "string",
      "start": "string",
      "start_datetime_local": "string",
      "start_datetime_utc": "string",
      "start_location": {},
      "status": "string",
      "trip_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `booker_id` | string |  |
| `end` | string |  |
| `end_datetime_local` | string |  |
| `end_datetime_utc` | string |  |
| `end_location` | object |  |
| `id` | string |  |
| `modified` | string |  |
| `start` | string |  |
| `start_datetime_local` | string |  |
| `start_datetime_utc` | string |  |
| `start_location` | object |  |
| `status` | string |  |
| `trip_name` | string |  |

## Native endpoint

Through the native TravelPerk API, this operation is `GET /trips/:tripId` (base URL `https://api.sandbox-travelperk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trip.md) for the provider-specific parameters and requirements.

