# Google Workspace Admin: Get User

Retrieves a user from Google Workspace Admin.

```
GET https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Workspace Admin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/get-user?connectionId=$CONNECTION_ID&userKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/get-user?${params}`, {
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
| `userKey` | string | yes | User primary email, alias, or unique ID. |

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
      "orgUnitPath": "string",
      "phones": [
        {
          "type": "string",
          "value": "string"
        }
      ],
      "primaryEmail": "ava@example.com",
      "recoveryPhone": "string",
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
| `emails[].address` | string |  |
| `emails[].primary` | boolean |  |
| `emails[].type` | string |  |
| `etag` | string |  |
| `id` | string |  |
| `includeInGlobalAddressList` | boolean |  |
| `ipWhitelisted` | boolean |  |
| `isAdmin` | boolean |  |
| `isDelegatedAdmin` | boolean |  |
| `isEnforcedIn2Sv` | boolean |  |
| `isEnrolledIn2Sv` | boolean |  |
| `isMailboxSetup` | boolean |  |
| `kind` | string |  |
| `languages[].languageCode` | string |  |
| `languages[].preference` | string |  |
| `lastLoginTime` | string |  |
| `name.familyName` | string |  |
| `name.fullName` | string |  |
| `name.givenName` | string |  |
| `orgUnitPath` | string |  |
| `phones[].type` | string |  |
| `phones[].value` | string |  |
| `primaryEmail` | string |  |
| `recoveryPhone` | string |  |
| `suspended` | boolean |  |
| `thumbnailPhotoEtag` | string |  |
| `thumbnailPhotoUrl` | string |  |

## Native endpoint

Through the native Google Workspace Admin API, this operation is `GET /admin/directory/v1/users/:userKey` (base URL `https://admin.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

