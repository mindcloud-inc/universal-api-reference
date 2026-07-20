# DocuWriter.ai Universal API Examples

These examples use the MindCloud API key and DocuWriter.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Spaces



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/list-spaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/list-spaces?${params}`, {
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
      "id": 1,
      "isPublic": true,
      "itemsCount": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Spaces action reference](actions/list-spaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docuWriterai/latest/actions/list-spaces).

## Create Space



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/create-space" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/create-space', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "id": 1,
      "isPublic": true,
      "name": "Ava Chen",
      "slug": "string",
      "sort": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Space action reference](actions/create-space.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docuWriterai/latest/actions/create-space).
