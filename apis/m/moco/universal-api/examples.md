# Moco Universal API Examples

These examples use the MindCloud API key and Moco connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Profile



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moco/latest/actions/get-profile?${params}`, {
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
      "avatarUrl": {},
      "createdAt": "string",
      "email": "ava@example.com",
      "external": true,
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": 1,
      "lastName": "Chen",
      "unit": {
        "id": 1,
        "name": "Ava Chen"
      },
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Profile action reference](actions/get-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moco/latest/actions/get-profile).

## Create Activity



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moco/latest/actions/create-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moco/latest/actions/create-activity', {
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
      "billable": true,
      "billed": true,
      "createdAt": "string",
      "customer": {
        "id": 1,
        "name": "Ava Chen"
      },
      "date": "string",
      "description": "string",
      "hourlyRate": 1,
      "hours": 1,
      "id": 1,
      "invoiceId": {},
      "project": {
        "billable": true,
        "id": 1,
        "name": "Ava Chen"
      },
      "remoteId": {},
      "remoteService": "string",
      "remoteUrl": {},
      "seconds": 1,
      "tag": "string",
      "task": {
        "billable": true,
        "id": 1,
        "name": "Ava Chen"
      },
      "timerStartedAt": {},
      "updatedAt": "string",
      "user": {
        "firstname": "Ava",
        "id": 1,
        "lastname": "Chen"
      },
      "workedSeconds": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Activity action reference](actions/create-activity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moco/latest/actions/create-activity).
