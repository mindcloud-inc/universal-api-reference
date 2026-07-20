# Shuffll: Create Asset Folder

Creates a new asset folder in Shuffll.

```
POST https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/create-asset-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/create-asset-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "newName": "Ava Chen",
  "organizationId": "69cac8104c4a701fd26271a1",
  "workspaceId": "69cac8104c4a701fd26271a5"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/create-asset-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "newName": "Ava Chen",
    "organizationId": "69cac8104c4a701fd26271a1",
    "workspaceId": "69cac8104c4a701fd26271a5"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `newName` | string | yes | New folder name. |
| `organizationId` | string | yes | Shuffll organization id. Default: `69cac8104c4a701fd26271a1`. |
| `workspaceId` | string | yes | Shuffll workspace id. Default: `69cac8104c4a701fd26271a5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the folder was created. |

## Native endpoint

Through the native Shuffll API, this operation is `POST /auth/organization/:organizationId/workspace/:workspaceId/assets/folder` (base URL `https://api.shuffll.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-asset-folder.md) for the provider-specific parameters and requirements.

