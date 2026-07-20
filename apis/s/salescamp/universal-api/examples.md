# Salescamp Universal API Examples

These examples use the MindCloud API key and Salescamp connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Collections



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/list-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/list-collections?${params}`, {
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
      "fieldCounts": 1,
      "id": "string",
      "isSystem": true,
      "label": "string",
      "name": "Ava Chen",
      "type": 1
    }
  ],
  "meta": {}
}
```

See the full [List Collections action reference](actions/list-collections.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salescamp/latest/actions/list-collections).

## Add Activity to Item



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/add-activity-to-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "itemId": "string",
  "action": "string",
  "title": "string",
  "date": "string",
  "time": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salescamp/latest/actions/add-activity-to-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "itemId": "string",
    "action": "string",
    "title": "string",
    "date": "string",
    "time": "string"
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
      "action": 1,
      "createdBy": "string",
      "createdOn": "string",
      "date": "string",
      "description": "string",
      "id": "string",
      "time": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Activity to Item action reference](actions/add-activity-to-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salescamp/latest/actions/add-activity-to-item).
