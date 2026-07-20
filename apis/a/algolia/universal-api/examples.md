# Algolia Universal API Examples

These examples use the MindCloud API key and Algolia connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List API keys

Retrieves all API keys from Algolia.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/list-api-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algolia/latest/actions/list-api-keys?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List API keys action reference](actions/list-api-keys.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/algolia/latest/actions/list-api-keys).

## Add a New Record

Creates a new record in an Algolia index.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/add-a-new-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "indexName": "Ava Chen",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/algolia/latest/actions/add-a-new-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "indexName": "Ava Chen",
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
      "objectID": "string",
      "taskID": 1
    }
  ],
  "meta": {}
}
```

See the full [Add a New Record action reference](actions/add-a-new-record.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/algolia/latest/actions/add-a-new-record).
