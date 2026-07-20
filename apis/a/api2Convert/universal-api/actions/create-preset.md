# Api2Convert: Create Preset

Creates a new preset in Api2Convert.

```
POST https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/create-preset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Api2Convert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/create-preset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "target": "string",
  "scope": "0",
  "options": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/create-preset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "target": "string",
    "scope": "0",
    "options": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name for the preset. |
| `target` | string | yes | Conversion target for the preset. |
| `scope` | string | yes | Preset visibility scope. One of: `0`, `1`. |
| `options` | object | yes | Conversion options to store in the preset. |

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

Through the native Api2Convert API, this operation is `POST /presets` (base URL `https://api.api2convert.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-preset.md) for the provider-specific parameters and requirements.

