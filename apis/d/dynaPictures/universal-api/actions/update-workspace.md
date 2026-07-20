# DynaPictures: Update Workspace

Updates an existing workspace in DynaPictures.

```
PUT https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/update-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DynaPictures `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/update-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/update-workspace', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the workspace to update. |
| `name` | string | yes | New name for the workspace. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DynaPictures API returns.

## Native endpoint

Through the native DynaPictures API, this operation is `PUT /workspaces/:id` (base URL `https://api.dynapictures.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workspace.md) for the provider-specific parameters and requirements.

