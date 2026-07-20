# Walla Form: Download Project Responses



```
GET https://connect.mindcloud.co/v1/universal/wallaForm/latest/actions/download-project-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walla Form `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wallaForm/latest/actions/download-project-responses?connectionId=$CONNECTION_ID&workspaceKey=string&projectKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceKey": "string",
  "projectKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wallaForm/latest/actions/download-project-responses?${params}`, {
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
| `workspaceKey` | string | yes | The Walla workspace key. |
| `projectKey` | string | yes | The Walla project key. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Walla Form API returns.

## Native endpoint

Through the native Walla Form API, this operation is `GET /workspace/:workspaceKey/project/:projectKey/response/list` (base URL `https://walla-api.data-lab.workers.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-project-responses.md) for the provider-specific parameters and requirements.

