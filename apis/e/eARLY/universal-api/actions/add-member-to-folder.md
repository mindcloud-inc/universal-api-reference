# EARLY: Add Member to Folder

Adds a member to an EARLY folder.

```
POST https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/add-member-to-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EARLY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/add-member-to-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderId": "340665",
  "email": "apps@mindcloud.co",
  "accessLevel": "full"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/add-member-to-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderId": "340665",
    "email": "apps@mindcloud.co",
    "accessLevel": "full"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | yes | Folder ID. Default: `340665`. |
| `email` | string | yes | Email address of the member to add. Default: `apps@mindcloud.co`. |
| `accessLevel` | string | yes | Folder access level. Default: `full`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EARLY API returns.

## Native endpoint

Through the native EARLY API, this operation is `POST /api/v4/folders/:folderId/members` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-member-to-folder.md) for the provider-specific parameters and requirements.

