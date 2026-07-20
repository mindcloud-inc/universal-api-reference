# Codemagic Universal API Examples

These examples use the MindCloud API key and Codemagic connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authenticated User

Retrieves the authenticated user from Codemagic.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-authenticated-user?${params}`, {
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
      "avatar_url": "https://example.com",
      "id": "string",
      "permissions": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Authenticated User action reference](actions/get-authenticated-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/codemagic/latest/actions/get-authenticated-user).

## Bulk Import Tester Group Contacts

Bulk imports contacts into a Codemagic tester group.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/bulk-import-tester-group-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "testerGroupId": "string",
  "emails[]": [
    "ava@example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/bulk-import-tester-group-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "testerGroupId": "string",
    "emails[]": ["ava@example.com"]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Bulk Import Tester Group Contacts action reference](actions/bulk-import-tester-group-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/codemagic/latest/actions/bulk-import-tester-group-contacts).
