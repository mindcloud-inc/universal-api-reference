# Digital Humani Universal API Examples

These examples use the MindCloud API key and Digital Humani connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authenticated User

Retrieves the authenticated user from Digital Humani.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/get-authenticated-user?${params}`, {
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
      "email": "ava@example.com",
      "enterpriseId": "string",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Authenticated User action reference](actions/get-authenticated-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/digitalHumani/latest/actions/get-authenticated-user).

## Plant Trees

Creates a tree-planting request in Digital Humani.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/plant-trees" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "treeCount": 1,
  "user": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digitalHumani/latest/actions/plant-trees', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "treeCount": 1,
    "user": "string"
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
      "created": "2026-05-07T12:00:00.000Z",
      "enterpriseId": "string",
      "projectId": "string",
      "treeCount": 1,
      "user": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Plant Trees action reference](actions/plant-trees.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/digitalHumani/latest/actions/plant-trees).
