# DynaPictures: Upload Asset

Uploads an asset to a DynaPictures workspace.

```
POST https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/upload-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DynaPictures `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/upload-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/upload-asset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Image file to upload. |
| `workspaceId` | string | yes | ID of the workspace to upload the asset into. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DynaPictures API returns.

## Native endpoint

Through the native DynaPictures API, this operation is `POST /media/:workspaceId/assets` (base URL `https://api.dynapictures.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-asset.md) for the provider-specific parameters and requirements.

