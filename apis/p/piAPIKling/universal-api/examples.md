# PiAPI/Kling Universal API Examples

These examples use the MindCloud API key and PiAPI/Kling connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/get-account-info?${params}`, {
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
      "accountGroup": "string",
      "accountMjBotGroupRelations": [
        {}
      ],
      "accountMjWorkerNodeGroupRelations": [
        {}
      ],
      "accountTags": [
        "string"
      ],
      "createdAt": "string",
      "creditPackInfo": {},
      "equivalentInUsd": 1,
      "id": 1,
      "isEnable": true,
      "isVerified": true,
      "klingFailoverEnabled": true,
      "lumaFailoverEnabled": true,
      "maxConcurrentTaskCount": 1,
      "mjFailoverEnabled": true,
      "name": "Ava Chen",
      "notificationHookUrl": "https://example.com",
      "plan": "string",
      "platform": "string",
      "sunoFailoverEnabled": true,
      "type": "string",
      "updatedAt": "string",
      "wallet": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIKling/latest/actions/get-account-info).

## Generate Avatar Video



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/generate-avatar-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.imageUrl": "https://example.com",
  "input.localDubbingUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIKling/latest/actions/generate-avatar-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.imageUrl": "https://example.com",
    "input.localDubbingUrl": "https://example.com"
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
      "config": {},
      "detail": {},
      "error": {},
      "input": {},
      "logs": [
        {}
      ],
      "meta": {},
      "model": "string",
      "output": {},
      "status": "string",
      "taskId": "string",
      "taskType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Generate Avatar Video action reference](actions/generate-avatar-video.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIKling/latest/actions/generate-avatar-video).
