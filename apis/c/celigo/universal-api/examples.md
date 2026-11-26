# Celigo Universal API Examples

These examples use the MindCloud API key and Celigo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Token Info



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-token-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-token-info?${params}`, {
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
      "byUser": {
        "accessLevel": "string",
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "environment": {
        "envUserId": "string",
        "id": "string",
        "name": "Ava Chen"
      },
      "ownerUser": {
        "company": "string",
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "token": {
        "autoPurgeAt": "2026-05-07T12:00:00.000Z",
        "fullAccess": true,
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Token Info action reference](actions/get-token-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/celigo/latest/actions/get-token-info).

## Cancel Job



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/cancel-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "6798e7a330f8f5fb4c2ee2fb"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/celigo/latest/actions/cancel-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "6798e7a330f8f5fb4c2ee2fb"
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

See the full [Cancel Job action reference](actions/cancel-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/celigo/latest/actions/cancel-job).
