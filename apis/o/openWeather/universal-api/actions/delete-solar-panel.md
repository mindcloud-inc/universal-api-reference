# OpenWeather: Delete Solar Panel

Deletes a solar panel from OpenWeather.

```
DELETE https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/delete-solar-panel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/delete-solar-panel?connectionId=$CONNECTION_ID&panelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "panelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openWeather/latest/actions/delete-solar-panel?${params}`, {
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
| `panelId` | string | yes | Solar panel identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "panel_id": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `panel_id` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native OpenWeather API, this operation is `DELETE https://api.openweathermap.org/energy/2.0/panel/:panelId` (base URL `https://api.openweathermap.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-solar-panel.md) for the provider-specific parameters and requirements.

