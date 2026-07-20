# Twist Universal API Examples

These examples use the MindCloud API key and Twist connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current authenticated user from Twist.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twist/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twist/latest/actions/get-current-user?${params}`, {
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
      "avatarUrls": {
        "s195": "https://example.com",
        "s35": "https://example.com",
        "s60": "https://example.com",
        "s640": "https://example.com"
      },
      "bot": true,
      "clientId": "string",
      "dateFormat": "string",
      "defaultWorkspace": 1,
      "email": "ava@example.com",
      "emails": [
        {
          "email": "ava@example.com",
          "primary": true
        }
      ],
      "featureIdentifier": "string",
      "firstName": "Ava",
      "id": 1,
      "lang": "string",
      "name": "Ava Chen",
      "removed": true,
      "restricted": true,
      "scheduledBanners": [
        "string"
      ],
      "setupPending": true,
      "shortName": "Ava Chen",
      "snoozed": true,
      "theme": "string",
      "timeFormat": "string",
      "timezone": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/twist/latest/actions/get-current-user).

## Archive Channel

Archives an existing channel in Twist.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/twist/latest/actions/archive-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twist/latest/actions/archive-channel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": 1
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

See the full [Archive Channel action reference](actions/archive-channel.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/twist/latest/actions/archive-channel).
