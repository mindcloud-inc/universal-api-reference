# Qlik Universal API Examples

These examples use the MindCloud API key and Qlik connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Qlik.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qlik/latest/actions/get-current-user?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "subject": "string",
      "tenantId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/qlik/latest/actions/get-current-user).

## Add Item To Collection

Adds an item to a collection in Qlik.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/add-item-to-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "65b8f2a1f4b0c2d3e4f56789",
  "id": "65b8f2a1f4b0c2d3e4f56789"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qlik/latest/actions/add-item-to-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "65b8f2a1f4b0c2d3e4f56789",
    "id": "65b8f2a1f4b0c2d3e4f56789"
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
      "id": "string",
      "name": "Ava Chen",
      "ownerId": "string",
      "resourceType": "string",
      "spaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Item To Collection action reference](actions/add-item-to-collection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/qlik/latest/actions/add-item-to-collection).
