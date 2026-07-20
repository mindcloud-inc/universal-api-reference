# CloudConvert Universal API Examples

These examples use the MindCloud API key and CloudConvert connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from CloudConvert.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/get-current-user?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "credits": 1,
      "email": "ava@example.com",
      "id": 1,
      "links": {
        "self": "https://example.com"
      },
      "paying": true,
      "taskRegion": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudConvert/latest/actions/get-current-user).

## Cancel Task

Cancels a task in your CloudConvert account.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/cancel-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudConvert/latest/actions/cancel-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "code": "string",
      "copyOfTaskId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "credits": 1,
      "endedAt": "2026-05-07T12:00:00.000Z",
      "hostName": "Ava Chen",
      "id": "string",
      "jobId": "string",
      "links": {
        "self": "https://example.com"
      },
      "message": "string",
      "operation": "string",
      "percent": 1,
      "priority": 1,
      "region": "string",
      "result": {
        "form": {
          "parameters": {
            "acl": "string",
            "key": "string",
            "policy": "string",
            "successActionStatus": "string",
            "xAmzAlgorithm": "string",
            "xAmzCredential": "string",
            "xAmzDate": "string",
            "xAmzSignature": "string"
          },
          "url": "https://example.com"
        }
      },
      "retryOfTaskId": "string",
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "storage": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

See the full [Cancel Task action reference](actions/cancel-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudConvert/latest/actions/cancel-task).
