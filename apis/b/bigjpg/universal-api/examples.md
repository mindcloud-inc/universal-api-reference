# Bigjpg Universal API Examples

These examples use the MindCloud API key and Bigjpg connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Task Result

Retrieves task results from Bigjpg by task ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigjpg/latest/actions/get-task-result?connectionId=$CONNECTION_ID&taskIds=tid1%2Ctid2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskIds": "tid1,tid2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigjpg/latest/actions/get-task-result?${params}`, {
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
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Task Result action reference](actions/get-task-result.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bigjpg/latest/actions/get-task-result).

## Create Enlarge Task

Creates an image enlargement task in Bigjpg.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bigjpg/latest/actions/create-enlarge-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "https://example.com/image.jpg",
  "style": "art",
  "noise": "3",
  "x2": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bigjpg/latest/actions/create-enlarge-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": "https://example.com/image.jpg",
    "style": "art",
    "noise": "3",
    "x2": "1"
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
      "status": "string",
      "tid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Enlarge Task action reference](actions/create-enlarge-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bigjpg/latest/actions/create-enlarge-task).
