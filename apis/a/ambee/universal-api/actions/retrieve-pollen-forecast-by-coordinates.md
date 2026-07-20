# Ambee: Retrieve Pollen Forecast By Coordinates

Retrieves pollen forecasts in Ambee by coordinates.

```
GET https://connect.mindcloud.co/v1/universal/ambee/latest/actions/retrieve-pollen-forecast-by-coordinates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ambee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ambee/latest/actions/retrieve-pollen-forecast-by-coordinates?connectionId=$CONNECTION_ID&lat=1&lng=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "1",
  "lng": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ambee/latest/actions/retrieve-pollen-forecast-by-coordinates?${params}`, {
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
| `lat` | number | yes |  |
| `lng` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ambee API returns.

## Native endpoint

Through the native Ambee API, this operation is `GET /forecast/pollen/by-lat-lng` (base URL `https://api.ambeedata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-pollen-forecast-by-coordinates.md) for the provider-specific parameters and requirements.

