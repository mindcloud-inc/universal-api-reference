# Pumble Universal API Examples

These examples use the MindCloud API key and Pumble connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves current user details from Pumble.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pumble/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pumble/latest/actions/get-current-user?${params}`, {
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
      "activeUntil": 1,
      "automaticallyTimeZone": true,
      "avatar": {
        "fullPath": "string",
        "scaledPath": "string"
      },
      "email": "ava@example.com",
      "id": "string",
      "isAddonBot": true,
      "isPumbleBot": true,
      "name": "Ava Chen",
      "phone": "string",
      "role": "string",
      "status": "string",
      "timeZoneId": "string",
      "title": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pumble/latest/actions/get-current-user).

## Add Reaction to Message

Adds a reaction to a Pumble message.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pumble/latest/actions/add-reaction-to-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pumble/latest/actions/add-reaction-to-message', {
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Reaction to Message action reference](actions/add-reaction-to-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pumble/latest/actions/add-reaction-to-message).
