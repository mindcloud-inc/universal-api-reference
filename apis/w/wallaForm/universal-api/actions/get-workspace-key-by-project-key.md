# Walla Form: Get Workspace Key by Project Key



```
GET https://connect.mindcloud.co/v1/universal/wallaForm/latest/actions/get-workspace-key-by-project-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walla Form `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wallaForm/latest/actions/get-workspace-key-by-project-key?connectionId=$CONNECTION_ID&projectKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wallaForm/latest/actions/get-workspace-key-by-project-key?${params}`, {
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
| `projectKey` | string | yes | The Walla project key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "workspaceKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `workspaceKey` | string |  |

## Native endpoint

Through the native Walla Form API, this operation is `GET /workspace/query/projectKey` (base URL `https://walla-api.data-lab.workers.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-key-by-project-key.md) for the provider-specific parameters and requirements.

