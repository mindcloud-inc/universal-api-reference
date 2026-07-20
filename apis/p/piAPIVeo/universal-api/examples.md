# PiAPI/Veo Universal API Examples

These examples use the MindCloud API key and PiAPI/Veo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves account information from PiAPI/Veo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIVeo/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIVeo/latest/actions/get-account-info?${params}`, {
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
      "code": 1,
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIVeo/latest/actions/get-account-info).

## Create Veo3 Image to Video Task

Creates a Veo 3 image-to-video task in PiAPI/Veo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIVeo/latest/actions/create-veo3-image-to-video-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.imageUrl": "https://example.com",
  "input.prompt": "string",
  "taskType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIVeo/latest/actions/create-veo3-image-to-video-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.imageUrl": "https://example.com",
    "input.prompt": "string",
    "taskType": "string"
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
        "status": "string",
        "task_id": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Veo3 Image to Video Task action reference](actions/create-veo3-image-to-video-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIVeo/latest/actions/create-veo3-image-to-video-task).
