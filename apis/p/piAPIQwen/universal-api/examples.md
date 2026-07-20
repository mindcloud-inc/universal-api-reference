# PiAPI/Qwen Universal API Examples

These examples use the MindCloud API key and PiAPI/Qwen connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Task

Retrieves task status details from PiAPI/Qwen.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIQwen/latest/actions/get-task?connectionId=$CONNECTION_ID&task_id=task-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "task_id": "task-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIQwen/latest/actions/get-task?${params}`, {
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
      "data": {
        "model": "string",
        "output": {
          "image_url": "https://example.com"
        },
        "status": "string",
        "task_id": "string",
        "task_type": "string"
      },
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Task action reference](actions/get-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIQwen/latest/actions/get-task).

## Create Image Edit Task

Creates an image edit task in PiAPI/Qwen.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIQwen/latest/actions/create-image-edit-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.image1": "https://example.com/image1.png",
  "input.prompt": "Describe the edit you want"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIQwen/latest/actions/create-image-edit-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.image1": "https://example.com/image1.png",
    "input.prompt": "Describe the edit you want"
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
        "model": "string",
        "status": "string",
        "task_id": "string",
        "task_type": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Image Edit Task action reference](actions/create-image-edit-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIQwen/latest/actions/create-image-edit-task).
