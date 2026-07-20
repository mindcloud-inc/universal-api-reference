# Claid AI Universal API Examples

These examples use the MindCloud API key and Claid AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Storage Types

Retrieves supported storage types from Claid AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/list-storage-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/list-storage-types?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Storage Types action reference](actions/list-storage-types.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/claidAI/latest/actions/list-storage-types).

## Create Scene

Creates a scene in Claid AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/create-scene" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "object": {},
  "scene": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/create-scene', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "object": {},
    "scene": {}
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
      "input": {},
      "output": [
        {}
      ],
      "profiling": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Scene action reference](actions/create-scene.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/claidAI/latest/actions/create-scene).
