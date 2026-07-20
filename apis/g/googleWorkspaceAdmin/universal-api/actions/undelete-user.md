# Google Workspace Admin: Undelete User

Restores a deleted user in Google Workspace Admin.

```
PUT https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/undelete-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/undelete-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userKey": "string",
  "orgUnitPath": "/"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/undelete-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userKey": "string",
    "orgUnitPath": "/"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userKey` | string | yes | The immutable unique ID of the deleted user to restore. |
| `orgUnitPath` | string | yes | The organizational unit path for the restored user. Default: `/`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Workspace Admin API returns.

## Native endpoint

Through the native Google Workspace Admin API, this operation is `POST /admin/directory/v1/users/:userKey/undelete` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/undelete-user.md) for the provider-specific parameters and requirements.

