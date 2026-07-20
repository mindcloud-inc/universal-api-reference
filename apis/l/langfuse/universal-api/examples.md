# Langfuse Universal API Examples

These examples use the MindCloud API key and Langfuse connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Project

Retrieves the project associated with your Langfuse API key.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/get-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/get-project?${params}`, {
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
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "organization": {
        "id": "string",
        "name": "Ava Chen"
      },
      "retentionDays": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Project action reference](actions/get-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/langfuse/latest/actions/get-project).

## Create Annotation Queue

Creates an annotation queue in Langfuse.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/create-annotation-queue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/create-annotation-queue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "scoreConfigIds": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Annotation Queue action reference](actions/create-annotation-queue.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/langfuse/latest/actions/create-annotation-queue).
