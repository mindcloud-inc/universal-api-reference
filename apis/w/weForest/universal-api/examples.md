# WeForest Universal API Examples

These examples use the MindCloud API key and WeForest connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get all users

Retrieves all user records from WeForest.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-all-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weForest/latest/actions/get-all-users?${params}`, {
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
      "customerId": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "role": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get all users action reference](actions/get-all-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/weForest/latest/actions/get-all-users).

## Add item(s) to tree-planting order

Adds items to a tree-planting order in WeForest.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weForest/latest/actions/add-item-s-to-tree-planting-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "items[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weForest/latest/actions/add-item-s-to-tree-planting-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "items[]": [{}]
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
      "customerId": 1,
      "endUser": {},
      "id": 1,
      "items": [
        {}
      ],
      "paid": true
    }
  ],
  "meta": {}
}
```

See the full [Add item(s) to tree-planting order action reference](actions/add-item-s-to-tree-planting-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/weForest/latest/actions/add-item-s-to-tree-planting-order).
