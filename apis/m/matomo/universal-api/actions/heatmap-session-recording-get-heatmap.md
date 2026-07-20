# Matomo: HeatmapSessionRecording get Heatmap



```
GET https://connect.mindcloud.co/v1/universal/matomo/latest/actions/heatmap-session-recording-get-heatmap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/heatmap-session-recording-get-heatmap?connectionId=$CONNECTION_ID&idSite=1&idSiteHsr=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idSite": "1",
  "idSiteHsr": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matomo/latest/actions/heatmap-session-recording-get-heatmap?${params}`, {
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
| `idSite` | number | yes | Matomo API parameter. Default: `1`. |
| `idSiteHsr` | number | yes | Matomo API parameter. |

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

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/heatmap-session-recording-get-heatmap.md) for the provider-specific parameters and requirements.

