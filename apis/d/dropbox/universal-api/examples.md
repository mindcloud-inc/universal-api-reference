# Dropbox Universal API Examples

These examples use the MindCloud API key and Dropbox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Account

Retrieves the current account details from Dropbox.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/get-current-account?${params}`, {
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
      "accountId": "string",
      "accountType": {
        "tag": "string"
      },
      "country": "string",
      "disabled": true,
      "email": "ava@example.com",
      "emailVerified": true,
      "isPaired": true,
      "locale": "string",
      "name": {
        "abbreviatedName": "Ava Chen",
        "displayName": "Ava Chen",
        "familiarName": "Ava Chen",
        "givenName": "Ava Chen",
        "surname": "Ava Chen"
      },
      "referralLink": "https://example.com",
      "rootInfo": {
        "homeNamespaceId": "Ava Chen",
        "rootNamespaceId": "Ava Chen",
        "tag": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Current Account action reference](actions/get-current-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dropbox/latest/actions/get-current-account).

## Add File Members

Adds members to a shared file in Dropbox.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/add-file-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "/Codex Dropbox Fixtures/share-target.txt",
  "memberEmails[]": "apps+dropbox-collab@mindcloud.co"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/add-file-members', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "/Codex Dropbox Fixtures/share-target.txt",
    "memberEmails[]": "apps+dropbox-collab@mindcloud.co"
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
      "invitationSignature": [
        "string"
      ],
      "member": {
        "email": "ava@example.com",
        "tag": "string"
      },
      "result": {
        "success": {
          "tag": "string"
        },
        "tag": "string"
      },
      "sckeySha1": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add File Members action reference](actions/add-file-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dropbox/latest/actions/add-file-members).
