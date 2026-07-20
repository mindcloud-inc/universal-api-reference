# Grafana: Export Alert Rule Group

Exports an alert rule group from Grafana.

```
GET https://connect.mindcloud.co/v1/universal/grafana/latest/actions/export-alert-rule-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grafana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grafana/latest/actions/export-alert-rule-group?connectionId=$CONNECTION_ID&folderUid=string&group=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderUid": "string",
  "group": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grafana/latest/actions/export-alert-rule-group?${params}`, {
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
| `folderUid` | string | yes | The folder UID. |
| `group` | string | yes | The alert rule group name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiVersion": 1,
      "folderUid": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | number |  |
| `folderUid` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Grafana API, this operation is `GET /v1/provisioning/folder/:FolderUID/rule-groups/:Group/export` (base URL `https://apps78aa.grafana.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-alert-rule-group.md) for the provider-specific parameters and requirements.

