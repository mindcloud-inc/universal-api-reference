# DynaPictures: Update Asset

Updates an asset in a DynaPictures workspace.

```
PUT https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/update-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DynaPictures `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/update-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "id": "string",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/update-asset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "id": "string",
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Replacement image file. |
| `id` | string | yes | ID of the asset to replace. |
| `workspaceId` | string | yes | ID of the workspace that owns the asset. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DynaPictures API returns.

## Native endpoint

Through the native DynaPictures API, this operation is `PUT /media/:workspaceId/assets/:id` (base URL `https://api.dynapictures.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-asset.md) for the provider-specific parameters and requirements.

