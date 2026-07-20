# Raindrop Universal API Examples

These examples use the MindCloud API key and Raindrop connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authenticated User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/get-authenticated-user?${params}`, {
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
      "result": true,
      "user": {
        "_id": 1,
        "avatar": "string",
        "email": "ava@example.com",
        "files": {
          "lastCheckPoint": "string",
          "size": 1,
          "used": 1
        },
        "fullName": "Ava Chen",
        "groups": [
          {}
        ],
        "lastAction": "string",
        "lastUpdate": "string",
        "lastVisit": "string",
        "name": "Ava Chen",
        "password": true,
        "pro": true,
        "registered": "string",
        "tfa": {
          "enabled": true
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Authenticated User action reference](actions/get-authenticated-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/raindrop/latest/actions/get-authenticated-user).

## Add Highlight



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/add-highlight" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/add-highlight', {
  method: 'PUT',
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
      "item": {
        "_id": 1,
        "highlights": [
          {
            "_id": "string",
            "color": "string",
            "created": "string",
            "lastUpdate": "string",
            "note": "string",
            "text": "string"
          }
        ]
      },
      "result": true
    }
  ],
  "meta": {}
}
```

See the full [Add Highlight action reference](actions/add-highlight.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/raindrop/latest/actions/add-highlight).
