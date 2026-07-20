# SigningHub: Move Package To Folder

Moves a package to a folder in SigningHub.

```
PUT https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/move-package-to-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/move-package-to-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "packageId": 1,
  "folderName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/move-package-to-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "packageId": 1,
    "folderName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `packageId` | number | yes | The document package to move. |
| `folderName` | string | yes | The destination custom or shared-space folder name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SigningHub API returns.

## Native endpoint

Through the native SigningHub API, this operation is `PUT /v4/packages/:packageId/move_to` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-package-to-folder.md) for the provider-specific parameters and requirements.

