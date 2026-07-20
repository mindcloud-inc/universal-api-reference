# Airlabs: List Flight Alert Listeners

Retrieves flight alert listeners from Airlabs.

```
GET https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-flight-alert-listeners
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airlabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-flight-alert-listeners?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-flight-alert-listeners?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "airline_iata": "string",
      "airline_icao": "string",
      "arr_date": "string",
      "arr_iata": "string",
      "arr_icao": "string",
      "arr_time": "string",
      "created": "string",
      "dep_date": "string",
      "dep_iata": "string",
      "dep_icao": "string",
      "dep_time": "string",
      "fields": "string",
      "flight_number": "string",
      "listener_id": 1,
      "webhook_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `airline_iata` | string | Airline IATA filter. |
| `airline_icao` | string | Airline ICAO filter. |
| `arr_date` | string | Arrival date filter. |
| `arr_iata` | string | Arrival airport IATA filter. |
| `arr_icao` | string | Arrival airport ICAO filter. |
| `arr_time` | string | Arrival time filter. |
| `created` | string | Listener creation date. |
| `dep_date` | string | Departure date filter. |
| `dep_iata` | string | Departure airport IATA filter. |
| `dep_icao` | string | Departure airport ICAO filter. |
| `dep_time` | string | Departure time filter. |
| `fields` | string | Comma-separated listener fields. |
| `flight_number` | string | Flight number filter. |
| `listener_id` | number | AirLabs listener ID. |
| `webhook_url` | string | Webhook URL registered for the listener. |

## Native endpoint

Through the native Airlabs API, this operation is `GET /listeners` (base URL `https://airlabs.co/api/v9`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-flight-alert-listeners.md) for the provider-specific parameters and requirements.

