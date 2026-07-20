# PiAPI/Sora Universal API Examples

These examples use the MindCloud API key and PiAPI/Sora connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get PiAPI Account Info



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPISora/latest/actions/get-piapi-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPISora/latest/actions/get-piapi-account-info?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get PiAPI Account Info action reference](actions/get-piapi-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPISora/latest/actions/get-piapi-account-info).

## Create Sora2 Pro Text to Video Task



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPISora/latest/actions/create-sora2-pro-text-to-video-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.prompt": "A dramatic tracking shot of a red race car in heavy rain"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPISora/latest/actions/create-sora2-pro-text-to-video-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.prompt": "A dramatic tracking shot of a red race car in heavy rain"
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
      "code": 1,
      "data": {
        "error": {
          "code": 1,
          "message": "string",
          "raw_message": "string"
        },
        "input": {
          "aspect_ratio": "string",
          "duration": 1,
          "prompt": "string",
          "resolution": "string"
        },
        "meta": {
          "created_at": "2026-05-07T12:00:00.000Z",
          "ended_at": "2026-05-07T12:00:00.000Z",
          "is_using_private_pool": true,
          "started_at": "2026-05-07T12:00:00.000Z",
          "usage": {
            "consume": 1,
            "frozen": 1,
            "type": "string"
          }
        },
        "model": "string",
        "status": "string",
        "task_id": "string",
        "task_type": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Sora2 Pro Text to Video Task action reference](actions/create-sora2-pro-text-to-video-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPISora/latest/actions/create-sora2-pro-text-to-video-task).
