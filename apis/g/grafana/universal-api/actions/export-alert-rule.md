# Grafana: Export Alert Rule

Exports an alert rule from Grafana.

```
GET https://connect.mindcloud.co/v1/universal/grafana/latest/actions/export-alert-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grafana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grafana/latest/actions/export-alert-rule?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grafana/latest/actions/export-alert-rule?${params}`, {
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
| `uid` | string | yes | The alert rule UID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folderUid": "string",
      "title": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folderUid` | string |  |
| `title` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native Grafana API, this operation is `GET /v1/provisioning/alert-rules/:UID/export` (base URL `https://apps78aa.grafana.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-alert-rule.md) for the provider-specific parameters and requirements.

