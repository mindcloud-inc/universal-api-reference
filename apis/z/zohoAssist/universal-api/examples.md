# Zoho Assist Universal API Examples

These examples use the MindCloud API key and Zoho Assist connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Info

Gets details for the current Zoho Assist user.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/get-user-info?${params}`, {
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
      "departments": [
        {}
      ],
      "joinDomain": "string",
      "license": {},
      "multiOrgEnabled": true,
      "nightModeEnabled": true,
      "orgDetails": {},
      "preferredDepartment": "string",
      "role": {},
      "screenName": "Ava Chen",
      "userRole": 1,
      "zuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User Info action reference](actions/get-user-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoAssist/latest/actions/get-user-info).

## Create Session

Creates a remote support or screen sharing session in Zoho Assist.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/create-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/create-session', {
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
      "authkey": "string",
      "authtype": "string",
      "customerUrl": "https://example.com",
      "sessionId": "string",
      "technicianUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Session action reference](actions/create-session.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoAssist/latest/actions/create-session).
