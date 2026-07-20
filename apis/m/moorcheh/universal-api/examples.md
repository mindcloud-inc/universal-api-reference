# Moorcheh Universal API Examples

These examples use the MindCloud API key and Moorcheh connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Namespaces

Retrieves all namespaces in your Moorcheh account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/list-namespaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/list-namespaces?${params}`, {
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
      "namespaces": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "item_count": 1,
          "namespace_name": "Ava Chen",
          "type": "Ava Chen",
          "vector_dimension": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Namespaces action reference](actions/list-namespaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moorcheh/latest/actions/list-namespaces).

## Create Namespace

Creates a new namespace in Moorcheh.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/create-namespace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "namespace_name": "Ava Chen",
  "type": "text"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/create-namespace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "namespace_name": "Ava Chen",
    "type": "text"
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
      "message": "string",
      "namespace_name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Namespace action reference](actions/create-namespace.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moorcheh/latest/actions/create-namespace).
