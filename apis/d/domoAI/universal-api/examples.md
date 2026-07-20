# DomoAI Universal API Examples

These examples use the MindCloud API key and DomoAI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Task

Retrieves task status and outputs from DomoAI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/domoAI/latest/actions/get-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/domoAI/latest/actions/get-task?${params}`, {
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

See the full [Get Task action reference](actions/get-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/domoAI/latest/actions/get-task).

## Create Image to Video Task

Creates a new image-to-video task in DomoAI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/domoAI/latest/actions/create-image-to-video-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "animate-2.4-faster",
  "image.domoaiUri": "string",
  "seconds": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/domoAI/latest/actions/create-image-to-video-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "animate-2.4-faster",
    "image.domoaiUri": "string",
    "seconds": 1
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

See the full [Create Image to Video Task action reference](actions/create-image-to-video-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/domoAI/latest/actions/create-image-to-video-task).
