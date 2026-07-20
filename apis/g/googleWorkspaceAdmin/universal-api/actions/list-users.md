# Google Workspace Admin: List Users

Retrieves users from Google Workspace Admin.

```
GET https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/list-users?connectionId=$CONNECTION_ID&customer=my_customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customer": "my_customer"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/list-users?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer` | string | yes | Workspace customer identifier. Keep `my_customer` for the current tenant unless you need a specific customer ID. Default: `my_customer`. Example: `my_customer`. |
| `maxResults` | number | no | Maximum users to return (up to 500). Default: `100`. Example: `100`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageToken` | string | no | Pagination token from previous response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "kind": "string",
      "nextPageToken": "string",
      "users": [
        {
          "agreedToTerms": true,
          "aliases": [
            "string"
          ],
          "archived": true,
          "changePasswordAtNextLogin": true,
          "creationTime": "string",
          "customerId": "string",
          "emails": [
            {
              "address": "ava@example.com",
              "primary": true,
              "type": "ava@example.com"
            }
          ],
          "etag": "string",
          "id": "string",
          "includeInGlobalAddressList": true,
          "ipWhitelisted": true,
          "isAdmin": true,
          "isDelegatedAdmin": true,
          "isEnforcedIn2Sv": true,
          "isEnrolledIn2Sv": true,
          "isGuestUser": true,
          "isMailboxSetup": true,
          "kind": "string",
          "languages": [
            {
              "languageCode": "string",
              "preference": "string"
            }
          ],
          "lastLoginTime": "string",
          "name": {
            "familyName": "Ava Chen",
            "fullName": "Ava Chen",
            "givenName": "Ava Chen"
          },
          "nonEditableAliases": [
            "string"
          ],
          "orgUnitPath": "string",
          "phones": [
            {
              "type": "string",
              "value": "string"
            }
          ],
          "primaryEmail": "ava@example.com",
          "recoveryEmail": "ava@example.com",
          "recoveryPhone": "string",
          "suspended": true,
          "thumbnailPhotoEtag": "string",
          "thumbnailPhotoUrl": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `kind` | string |  |
| `nextPageToken` | string | Pagination token for the next page of directory users. |
| `users[].agreedToTerms` | boolean |  |
| `users[].aliases[]` | string |  |
| `users[].archived` | boolean |  |
| `users[].changePasswordAtNextLogin` | boolean |  |
| `users[].creationTime` | string |  |
| `users[].customerId` | string |  |
| `users[].emails[].address` | string |  |
| `users[].emails[].primary` | boolean | Whether this email is the user's primary address. |
| `users[].emails[].type` | string |  |
| `users[].etag` | string |  |
| `users[].id` | string |  |
| `users[].includeInGlobalAddressList` | boolean |  |
| `users[].ipWhitelisted` | boolean |  |
| `users[].isAdmin` | boolean |  |
| `users[].isDelegatedAdmin` | boolean |  |
| `users[].isEnforcedIn2Sv` | boolean |  |
| `users[].isEnrolledIn2Sv` | boolean |  |
| `users[].isGuestUser` | boolean | Whether the directory user is a guest user. |
| `users[].isMailboxSetup` | boolean |  |
| `users[].kind` | string |  |
| `users[].languages[].languageCode` | string |  |
| `users[].languages[].preference` | string |  |
| `users[].lastLoginTime` | string |  |
| `users[].name.familyName` | string |  |
| `users[].name.fullName` | string |  |
| `users[].name.givenName` | string |  |
| `users[].nonEditableAliases[]` | string |  |
| `users[].orgUnitPath` | string |  |
| `users[].phones[].type` | string |  |
| `users[].phones[].value` | string |  |
| `users[].primaryEmail` | string |  |
| `users[].recoveryEmail` | string | Recovery email configured for the user, when available. |
| `users[].recoveryPhone` | string | Recovery phone configured for the user, when available. |
| `users[].suspended` | boolean |  |
| `users[].thumbnailPhotoEtag` | string |  |
| `users[].thumbnailPhotoUrl` | string |  |

## Native endpoint

Through the native Google Workspace Admin API, this operation is `GET /admin/directory/v1/users` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

