# Api2Convert: Get Preset

Retrieves a specific preset from Api2Convert.

```
GET https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-preset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-preset?connectionId=$CONNECTION_ID&presetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "presetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-preset?${params}`, {
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
| `presetId` | string | yes | Unique identifier of the preset to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "id": "string",
      "name": "Ava Chen",
      "options": {},
      "scope": "string",
      "target": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Preset category. |
| `id` | string | Preset identifier. |
| `name` | string | Preset name. |
| `options` | object | Preset options. |
| `scope` | string | Preset scope. |
| `target` | string | Preset target format. |

## Native endpoint

Through the native Api2Convert API, this operation is `GET /presets/:preset_id` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-preset.md) for the provider-specific parameters and requirements.

