# Dialpad Universal API Examples

These examples use the MindCloud API key and Dialpad connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Dialpad.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/get-current-user?${params}`, {
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
      "adminOfficeIds": [
        "string"
      ],
      "companyId": "string",
      "country": "string",
      "dateActive": "string",
      "dateAdded": "string",
      "displayName": "Ava Chen",
      "doNotDisturb": true,
      "emails": [
        "ava@example.com"
      ],
      "firstName": "Ava",
      "hasRbac": true,
      "id": "string",
      "imageUrl": "https://example.com",
      "internationalDialingEnabled": true,
      "isAdmin": true,
      "isAvailable": true,
      "isOnDuty": true,
      "isOnline": true,
      "isSuperAdmin": true,
      "language": "string",
      "lastName": "Chen",
      "license": "string",
      "muted": true,
      "officeId": "string",
      "onboardingCompleted": true,
      "phoneNumbers": [
        "string"
      ],
      "remoteService": "string",
      "state": "string",
      "timezone": "string",
      "voicemail": {
        "isDefaultVoicemail": true,
        "name": "ava@example.com",
        "voicemailNotificationsEnabled": true
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dialpad/latest/actions/get-current-user).

## Create Channel

Creates a new channel in Dialpad.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/create-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud Test Channel",
  "description": "Temporary test channel for MindCloud verification",
  "privacyType": "private"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/create-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud Test Channel",
    "description": "Temporary test channel for MindCloud verification",
    "privacyType": "private"
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
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Channel action reference](actions/create-channel.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dialpad/latest/actions/create-channel).
