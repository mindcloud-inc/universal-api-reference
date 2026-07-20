# Dynamic Mockups Universal API Examples

These examples use the MindCloud API key and Dynamic Mockups connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Collections

Retrieves your collections from Dynamic Mockups.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/list-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/list-collections?${params}`, {
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
      "data": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "createdAtTimestamp": "2026-05-07T12:00:00.000Z",
          "mockupCount": 1,
          "name": "Ava Chen",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "updatedAtTimestamp": "2026-05-07T12:00:00.000Z",
          "uuid": "string"
        }
      ],
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [List Collections action reference](actions/list-collections.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dynamicMockups/latest/actions/list-collections).

## Create Bulk Renders

Creates bulk renders from a Dynamic Mockups collection.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/create-bulk-renders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collection_uuid": "e.g. 0663101b-f01c-4e85-89af-f90b4e9f983b"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/create-bulk-renders', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collection_uuid": "e.g. 0663101b-f01c-4e85-89af-f90b4e9f983b"
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

See the full [Create Bulk Renders action reference](actions/create-bulk-renders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dynamicMockups/latest/actions/create-bulk-renders).
