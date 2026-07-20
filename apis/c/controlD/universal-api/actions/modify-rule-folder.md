# Control D: Modify Rule Folder

Updates a rule folder in Control D.

```
PUT https://connect.mindcloud.co/v1/universal/controlD/latest/actions/modify-rule-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Control D `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/modify-rule-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileId": "string",
  "folder": "string",
  "do": 1,
  "status": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/controlD/latest/actions/modify-rule-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileId": "string",
    "folder": "string",
    "do": 1,
    "status": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profileId` | string | yes | Primary key (PK) of the profile |
| `folder` | string | yes | Folder ID |
| `name` | string | no | Rename the folder to this name |
| `do` | number | yes | Add a rule type to a folder. All rules inside will inherit rule type |
| `via` | string | no | Add spoof IP or hostname, or proxy identifer if do=2 or do=3 |
| `status` | number | yes | Status of the folder and all rules inside |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Control D API returns.

## Native endpoint

Through the native Control D API, this operation is `PUT /profiles/:profileId/groups/:folder` (base URL `https://api.controld.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-rule-folder.md) for the provider-specific parameters and requirements.

