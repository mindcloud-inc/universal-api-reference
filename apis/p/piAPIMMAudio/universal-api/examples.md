# PiAPI/MMAudio Universal API Examples

These examples use the MindCloud API key and PiAPI/MMAudio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Task

Retrieves an MMAudio task from PiAPI/MMAudio.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIMMAudio/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=task%20identifier%20returned%20by%20Generate%20Audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "task identifier returned by Generate Audio"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIMMAudio/latest/actions/get-task?${params}`, {
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
      "input": "string",
      "metadata": {
        "createdAt": "string",
        "endedAt": "string",
        "quotaFrozen": 1,
        "quotaUsage": 1,
        "startedAt": "string"
      },
      "status": "string",
      "task": {
        "createTime": 1,
        "deleted": true,
        "favored": true,
        "id": 1,
        "status": 1,
        "type": "string",
        "updateTime": 1,
        "userId": 1
      },
      "taskId": "string",
      "works": [
        {
          "contentType": "string",
          "cover": {
            "resource": "string"
          },
          "deleted": true,
          "publishStatus": "string",
          "resource": {
            "duration": 1,
            "resource": "string",
            "resourceWithoutWatermark": "string"
          },
          "status": 1,
          "workId": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Task action reference](actions/get-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIMMAudio/latest/actions/get-task).

## Generate Audio

Creates an MMAudio audio generation task in PiAPI/MMAudio.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIMMAudio/latest/actions/generate-audio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.video": "https://example.com/video.mp4"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIMMAudio/latest/actions/generate-audio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.video": "https://example.com/video.mp4"
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
      "error": {
        "code": 1,
        "message": "string"
      },
      "meta": {
        "createdAt": "string",
        "endedAt": "string",
        "isUsingPrivatePool": true,
        "startedAt": "string",
        "usage": {
          "consume": 1,
          "frozen": 1,
          "type": "string"
        }
      },
      "model": "string",
      "status": "string",
      "taskId": "string",
      "taskType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Generate Audio action reference](actions/generate-audio.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIMMAudio/latest/actions/generate-audio).
