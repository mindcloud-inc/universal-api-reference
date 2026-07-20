# Rebrandly: Populate Preset

Populates a preset for a template in Rebrandly.

```
PUT https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/populate-preset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrandly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/populate-preset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "93a7720c6c684c2d91e3522d5672d7b5",
  "presetId": "89f1e8ebd4124fe9ad1653a012b6b434",
  "name": "MindCloud Stage 3 Preset",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/populate-preset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "93a7720c6c684c2d91e3522d5672d7b5",
    "presetId": "89f1e8ebd4124fe9ad1653a012b6b434",
    "name": "MindCloud Stage 3 Preset",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Template identifier returned by List Templates. Example: `93a7720c6c684c2d91e3522d5672d7b5`. |
| `presetId` | string | yes | Preset identifier returned by Create Preset or List Presets. Example: `89f1e8ebd4124fe9ad1653a012b6b434`. |
| `name` | string | yes | Human-friendly preset name. Example: `MindCloud Stage 3 Preset`. |
| `data` | object | yes | Preset data object containing a query object keyed by parameter ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rebrandly API returns.

## Native endpoint

Through the native Rebrandly API, this operation is `POST https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/presets/:presetId` (base URL `https://api.rebrandly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/populate-preset.md) for the provider-specific parameters and requirements.

