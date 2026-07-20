# Typesense: Upsert Preset

Creates or updates a search preset in Typesense.

```
PUT https://connect.mindcloud.co/v1/universal/typesense/latest/actions/upsert-preset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typesense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/typesense/latest/actions/upsert-preset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "preset": {},
  "presetName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typesense/latest/actions/upsert-preset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "preset": {},
    "presetName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `preset` | object | yes | Preset definition JSON body. |
| `presetName` | string | yes | Preset name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "response": {},
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `response` | object |  |
| `value` | object |  |

## Native endpoint

Through the native Typesense API, this operation is `PUT /presets/{{presetName}}` (base URL `https://5brh8vz1lictf0jop-1.a2.typesense.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-preset.md) for the provider-specific parameters and requirements.

