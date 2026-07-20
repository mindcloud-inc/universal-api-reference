# OpenWeather: Delete Solar Location

Deletes a solar location from OpenWeather.

```
DELETE https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/delete-solar-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/delete-solar-location?connectionId=$CONNECTION_ID&locationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/delete-solar-location?${params}`, {
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
| `locationId` | string | yes | Solar location identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "location_id": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `location_id` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native OpenWeather API, this operation is `DELETE https://api.openweathermap.org/energy/2.0/location/:locationId` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-solar-location.md) for the provider-specific parameters and requirements.

