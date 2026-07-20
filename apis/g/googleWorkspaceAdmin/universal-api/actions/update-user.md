# Google Workspace Admin: Update User

Updates an existing user in Google Workspace Admin.

```
PUT https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userKey` | string | yes | User primary email, alias, or unique ID. |
| `name.givenName` | string | no | Updated given name for the user. |
| `name.familyName` | string | no | Updated family name for the user. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `suspended` | boolean | no | Whether the user is suspended. |
| `changePasswordAtNextLogin` | boolean | no | Whether the user must change their password the next time they sign in. |
| `orgUnitPath` | string | no | Updated organizational unit path for the user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agreedToTerms": true,
      "archived": true,
      "changePasswordAtNextLogin": true,
      "creationTime": "string",
      "customerId": "string",
      "etag": "string",
      "id": "string",
      "includeInGlobalAddressList": true,
      "ipWhitelisted": true,
      "isAdmin": true,
      "isDelegatedAdmin": true,
      "isMailboxSetup": true,
      "kind": "string",
      "lastLoginTime": "string",
      "name": {
        "familyName": "Ava Chen",
        "givenName": "Ava Chen"
      },
      "orgUnitPath": "string",
      "primaryEmail": "ava@example.com",
      "recoveryEmail": "ava@example.com",
      "suspended": true,
      "thumbnailPhotoEtag": "string",
      "thumbnailPhotoUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agreedToTerms` | boolean |  |
| `archived` | boolean |  |
| `changePasswordAtNextLogin` | boolean |  |
| `creationTime` | string |  |
| `customerId` | string |  |
| `etag` | string |  |
| `id` | string |  |
| `includeInGlobalAddressList` | boolean |  |
| `ipWhitelisted` | boolean |  |
| `isAdmin` | boolean |  |
| `isDelegatedAdmin` | boolean |  |
| `isMailboxSetup` | boolean |  |
| `kind` | string |  |
| `lastLoginTime` | string |  |
| `name.familyName` | string |  |
| `name.givenName` | string |  |
| `orgUnitPath` | string |  |
| `primaryEmail` | string |  |
| `recoveryEmail` | string |  |
| `suspended` | boolean |  |
| `thumbnailPhotoEtag` | string |  |
| `thumbnailPhotoUrl` | string |  |

## Native endpoint

Through the native Google Workspace Admin API, this operation is `PUT /admin/directory/v1/users/:userKey` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

