# Google Workspace Admin: Create User

Creates a new user in Google Workspace Admin.

```
POST https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "primaryEmail": "ava@example.com",
  "password": "string",
  "name.givenName": "Ava Chen",
  "name.familyName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "primaryEmail": "ava@example.com",
    "password": "string",
    "name.givenName": "Ava Chen",
    "name.familyName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `primaryEmail` | string | yes | The user's primary email address. Must be unique and cannot be an alias of another user. |
| `password` | string | yes | ASCII password between 8 and 100 characters. |
| `name.givenName` | string | yes | The user's given name. |
| `name.familyName` | string | yes | The user's family name. |
| `changePasswordAtNextLogin` | boolean | no | Whether the user must change their password the next time they sign in. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orgUnitPath` | string | no | Optional organizational unit path for the new user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changePasswordAtNextLogin": true,
      "creationTime": "string",
      "customerId": "string",
      "etag": "string",
      "id": "string",
      "isAdmin": true,
      "isDelegatedAdmin": true,
      "isMailboxSetup": true,
      "kind": "string",
      "name": {
        "familyName": "Ava Chen",
        "givenName": "Ava Chen"
      },
      "orgUnitPath": "string",
      "primaryEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changePasswordAtNextLogin` | boolean |  |
| `creationTime` | string |  |
| `customerId` | string |  |
| `etag` | string |  |
| `id` | string |  |
| `isAdmin` | boolean |  |
| `isDelegatedAdmin` | boolean |  |
| `isMailboxSetup` | boolean |  |
| `kind` | string |  |
| `name.familyName` | string |  |
| `name.givenName` | string |  |
| `orgUnitPath` | string |  |
| `primaryEmail` | string |  |

## Native endpoint

Through the native Google Workspace Admin API, this operation is `POST /admin/directory/v1/users` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

