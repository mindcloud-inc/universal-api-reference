# 2Chat Universal API Examples

These examples use the MindCloud API key and 2Chat connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves your account details from 2Chat.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-account-info?${params}`, {
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
      "account": {
        "blocked": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "expiresAt": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "onTrial": true,
        "uuid": "string"
      },
      "limits": {
        "requestsPerMinute": 1
      },
      "success": true,
      "usage": {
        "apiRequestsAvailable": 1,
        "apiRequestsPlanDefault": 1,
        "numberCheckRequestsAvailable": 1,
        "numberCheckRequestsPlanDefault": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chat/latest/actions/get-account-info).

## Add Participant

Updates a WhatsApp group in 2Chat by adding participants.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chat/latest/actions/add-participant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "group_uuid": "string",
  "fromNumber": "string",
  "participants[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chat/latest/actions/add-participant', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "group_uuid": "string",
    "fromNumber": "string",
    "participants[]": ["string"]
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

See the full [Add Participant action reference](actions/add-participant.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chat/latest/actions/add-participant).
