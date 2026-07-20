# Resco Cloud: Export Project

Exports an app project definition from Resco Cloud.

```
GET https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/export-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resco Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/export-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rescoCloud/latest/actions/export-project?${params}`, {
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
| `projectId` | string | no | Project ID to export. Use either Project ID or Project Name. |
| `projectName` | string | no | Project name to export. Use either Project Name or Project ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Resco Cloud API returns.

## Native endpoint

Through the native Resco Cloud API, this operation is `POST /ExportProject` (base URL `https://{{credentials.organization}}.app.resco.net/rest/v1/data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-project.md) for the provider-specific parameters and requirements.

