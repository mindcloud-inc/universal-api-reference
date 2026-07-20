# Avoma Universal API Examples

These examples use the MindCloud API key and Avoma connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves users from Avoma.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-users?${params}`, {
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
      "active": true,
      "position": "string",
      "role": {
        "description": "string",
        "displayName": "Ava Chen",
        "name": "Ava Chen",
        "roleType": "string",
        "uuid": "string"
      },
      "status": "string",
      "user": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "isActive": true,
        "jobFunction": "string",
        "lastName": "Chen",
        "position": "string"
      },
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/avoma/latest/actions/list-users).

## Create Call

Creates a new call in Avoma.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/create-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "externalId": "string",
  "userEmail": "ava@example.com",
  "fromNumber": "string",
  "toNumber": "string",
  "startAt": "string",
  "recordingUrl": "https://example.com",
  "direction": "string",
  "source": "string",
  "participants[].email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avoma/latest/actions/create-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "externalId": "string",
    "userEmail": "ava@example.com",
    "fromNumber": "string",
    "toNumber": "string",
    "startAt": "string",
    "recordingUrl": "https://example.com",
    "direction": "string",
    "source": "string",
    "participants[].email": "ava@example.com"
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
      "additionalDetails": "string",
      "answered": true,
      "direction": "string",
      "endAt": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "frm": "string",
      "isVoicemail": true,
      "meeting": {
        "endAt": "2026-05-07T12:00:00.000Z",
        "organizerEmail": "ava@example.com",
        "startAt": "2026-05-07T12:00:00.000Z",
        "state": "string",
        "subject": "string",
        "uuid": "string"
      },
      "meetingOutcomeUuid": "string",
      "meetingPurposeUuid": "string",
      "organization": {
        "domain": "string",
        "name": "Ava Chen"
      },
      "recordingUrl": "https://example.com",
      "source": "string",
      "startAt": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "subject": "string",
      "to": "string",
      "userEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Call action reference](actions/create-call.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/avoma/latest/actions/create-call).
