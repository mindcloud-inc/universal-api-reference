# Aspera on Cloud: Update Workspace

Updates a workspace in Aspera on Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/update-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspera on Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/update-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "ws_123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asperaOnCloud/latest/actions/update-workspace', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "ws_123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the workspace. Example: `ws_123`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aspera on Cloud API returns.

## Native endpoint

Through the native Aspera on Cloud API, this operation is `PUT /v1/workspaces/{id}` (base URL `https://api.ibmaspera.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workspace.md) for the provider-specific parameters and requirements.

