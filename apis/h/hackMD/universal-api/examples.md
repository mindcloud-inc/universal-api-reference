# HackMD Universal API Examples

These examples use the MindCloud API key and HackMD connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hackMD/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hackMD/latest/actions/get-current-user?${params}`, {
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
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "photo": "string",
      "teams": [
        {}
      ],
      "upgraded": true,
      "userPath": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hackMD/latest/actions/get-current-user).

## Create Note



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hackMD/latest/actions/create-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hackMD/latest/actions/create-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "content": "string",
      "createdAt": 1,
      "description": "string",
      "id": "string",
      "lastChangedAt": 1,
      "lastChangeUser": {},
      "permalink": "https://example.com",
      "publishedAt": 1,
      "publishLink": "https://example.com",
      "publishType": "string",
      "readPermission": "string",
      "shortId": "string",
      "tags": [
        "string"
      ],
      "tagsUpdatedAt": 1,
      "teamPath": "string",
      "title": "string",
      "titleUpdatedAt": 1,
      "userPath": "string",
      "writePermission": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Note action reference](actions/create-note.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hackMD/latest/actions/create-note).
