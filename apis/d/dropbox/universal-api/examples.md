# Dropbox Universal API Examples

These examples use the MindCloud API key and Dropbox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Continue Folder Listing

Retrieves more Dropbox folder contents using a cursor.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/continue-folder-listing?connectionId=$CONNECTION_ID&cursor=ZtkX9_EHj3x7PMkVuFIhwKYXEpwpLwyxp9vMKomUhllil9q7eWiAu" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cursor": "ZtkX9_EHj3x7PMkVuFIhwKYXEpwpLwyxp9vMKomUhllil9q7eWiAu"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/continue-folder-listing?${params}`, {
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
      "cursor": "string",
      "hasMore": true
    }
  ],
  "meta": {}
}
```

See the full [Continue Folder Listing action reference](actions/continue-folder-listing.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dropbox/latest/actions/continue-folder-listing).

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
