# Google Workspace Admin Universal API Examples

These examples use the MindCloud API key and Google Workspace Admin connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves users from Google Workspace Admin.

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

Example response:

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

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleWorkspaceAdmin/latest/actions/list-users).

## Add Group Member

Adds a member to a Google Workspace Admin group.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/add-group-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "groupKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleWorkspaceAdmin/latest/actions/add-group-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "groupKey": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "deliverySettings": "string",
      "email": "ava@example.com",
      "etag": "string",
      "id": "string",
      "kind": "string",
      "role": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Group Member action reference](actions/add-group-member.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleWorkspaceAdmin/latest/actions/add-group-member).
