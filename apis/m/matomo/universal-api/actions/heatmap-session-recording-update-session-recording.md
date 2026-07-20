# Matomo: HeatmapSessionRecording update Session Recording



```
PUT https://connect.mindcloud.co/v1/universal/matomo/latest/actions/heatmap-session-recording-update-session-recording
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/heatmap-session-recording-update-session-recording" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idSite": "1",
  "idSiteHsr": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/matomo/latest/actions/heatmap-session-recording-update-session-recording', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idSite": "1",
    "idSiteHsr": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idSite` | number | yes | Matomo API parameter. Default: `1`. |
| `idSiteHsr` | number | yes | Matomo API parameter. |
| `name` | string | yes | Matomo API parameter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `matchPageRules` | boolean | no | Matomo API parameter. Default: `Array`. |
| `sampleLimit` | string | no | Matomo API parameter. Default: `1000`. |
| `sampleRate` | string | no | Matomo API parameter. Default: `10`. |
| `minSessionTime` | string | no | Matomo API parameter. Default: `0`. |
| `requiresActivity` | string | no | Matomo API parameter. Default: `1`. |
| `captureKeystrokes` | string | no | Matomo API parameter. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "label": "string",
      "nb_actions": 1,
      "nb_visits": 1,
      "result": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `label` | string | Matomo response label |
| `nb_actions` | number | Actions |
| `nb_visits` | number | Visits |
| `result` | string | Operation result |
| `value` | string | Matomo response value |

## Native endpoint

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/heatmap-session-recording-update-session-recording.md) for the provider-specific parameters and requirements.

