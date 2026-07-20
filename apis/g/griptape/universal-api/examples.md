# Griptape Universal API Examples

These examples use the MindCloud API key and Griptape connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Threads

Finds threads in Griptape.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-threads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-threads?${params}`, {
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
      "pagination": {
        "page_number": 1,
        "page_size": 1,
        "total_count": 1,
        "total_pages": 1
      },
      "threads": [
        {
          "alias": "string",
          "created_at": "string",
          "created_by": "string",
          "message_count": 1,
          "messages_length": 1,
          "metadata": {},
          "name": "Ava Chen",
          "organization_id": "string",
          "thread_id": "string",
          "updated_at": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Threads action reference](actions/list-threads.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/griptape/latest/actions/list-threads).

## Create Thread

Creates a new thread in Griptape.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/create-thread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/griptape/latest/actions/create-thread', {
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
      "alias": "string",
      "created_at": "string",
      "created_by": "string",
      "metadata": {},
      "name": "Ava Chen",
      "organization_id": "string",
      "thread_id": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Thread action reference](actions/create-thread.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/griptape/latest/actions/create-thread).
