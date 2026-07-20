# v0: Find Deployments

Finds deployments in the v0 workspace.

```
GET https://connect.mindcloud.co/v1/universal/v0/latest/actions/find-deployments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a v0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/v0/latest/actions/find-deployments?connectionId=$CONNECTION_ID&projectId=string&chatId=string&versionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "chatId": "string",
  "versionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/v0/latest/actions/find-deployments?${params}`, {
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
| `projectId` | string | yes | The ID of the project to find deployments for. |
| `chatId` | string | yes | The ID of the chat to find deployments for. |
| `versionId` | string | yes | The ID of the version to find deployments for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiUrl": "https://example.com",
      "chatId": "string",
      "id": "string",
      "inspectorUrl": "https://example.com",
      "object": "string",
      "projectId": "string",
      "versionId": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiUrl` | string |  |
| `chatId` | string |  |
| `id` | string |  |
| `inspectorUrl` | string |  |
| `object` | string |  |
| `projectId` | string |  |
| `versionId` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native v0 API, this operation is `GET /v1/deployments` (base URL `https://api.v0.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-deployments.md) for the provider-specific parameters and requirements.

