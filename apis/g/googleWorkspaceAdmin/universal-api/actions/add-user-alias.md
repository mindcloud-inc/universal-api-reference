# Google Workspace Admin: Add User Alias

Adds a user alias in Google Workspace Admin.

```
POST https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/add-user-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/add-user-alias" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userKey": "string",
  "alias": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/add-user-alias', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userKey": "string",
    "alias": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userKey` | string | yes | User primary email, alias, or unique ID. |
| `alias` | string | yes | New alias email address to add for the user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "etag": "string",
      "id": "string",
      "kind": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `etag` | string |  |
| `id` | string |  |
| `kind` | string |  |

## Native endpoint

Through the native Google Workspace Admin API, this operation is `POST /admin/directory/v1/users/:userKey/aliases` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user-alias.md) for the provider-specific parameters and requirements.

