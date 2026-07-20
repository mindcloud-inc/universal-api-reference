# PiAPI/Hunyuan Universal API Examples

These examples use the MindCloud API key and PiAPI/Hunyuan connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIHunyuan/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIHunyuan/latest/actions/get-account-info?${params}`, {
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
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditPackInfo": {},
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "equivalentInUsd": 1,
      "id": 1,
      "isEnable": true,
      "isUsingPrivateChatGptPool": true,
      "isUsingPrivateKlingPool": true,
      "isUsingPrivateLumaPool": true,
      "isUsingPrivateSunoPool": true,
      "isUsingPrivateUdioPool": true,
      "isVerified": true,
      "klingFailoverEnabled": true,
      "lumaFailoverEnabled": true,
      "maxConcurrentTaskCount": 1,
      "mjFailoverEnabled": true,
      "name": "Ava Chen",
      "notificationHookUrl": "https://example.com",
      "plan": "string",
      "platform": "string",
      "privatePoolSize": 1,
      "sunoFailoverEnabled": true,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "wallet": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIHunyuan/latest/actions/get-account-info).

## Create Fast Text to Video Task



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIHunyuan/latest/actions/create-fast-text-to-video-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIHunyuan/latest/actions/create-fast-text-to-video-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.prompt": "string"
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
      "output": {},
      "status": "string",
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Fast Text to Video Task action reference](actions/create-fast-text-to-video-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIHunyuan/latest/actions/create-fast-text-to-video-task).
