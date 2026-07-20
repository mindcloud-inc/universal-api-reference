# Sprinklr Universal API Examples

These examples use the MindCloud API key and Sprinklr connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Custom Entity Definitions

Retrieves custom entity definitions from Sprinklr.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/list-custom-entity-definitions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/list-custom-entity-definitions?${params}`, {
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
      "createdTime": 1,
      "id": "string",
      "modifiedTime": 1,
      "name": "Ava Chen",
      "pluralName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Custom Entity Definitions action reference](actions/list-custom-entity-definitions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sprinklr/latest/actions/list-custom-entity-definitions).

## Add Comment

Creates a comment in Sprinklr.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/add-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityId": "string",
  "entityType": "string",
  "requestBody": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sprinklr/latest/actions/add-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityId": "string",
    "entityType": "string",
    "requestBody": {}
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

See the full [Add Comment action reference](actions/add-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sprinklr/latest/actions/add-comment).
