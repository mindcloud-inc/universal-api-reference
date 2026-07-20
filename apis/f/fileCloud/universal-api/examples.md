# FileCloud Universal API Examples

These examples use the MindCloud API key and FileCloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Resource Types

Retrieves resource types from FileCloud.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/list-resource-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/list-resource-types?${params}`, {
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
      "Resources": [
        {}
      ],
      "schemas": [
        "string"
      ],
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

See the full [List Resource Types action reference](actions/list-resource-types.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fileCloud/latest/actions/list-resource-types).

## Create Group

Creates a new group in FileCloud.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/create-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "displayName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/create-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "displayName": "Ava Chen"
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
      "displayName": "Ava Chen",
      "id": "string",
      "members": [
        {}
      ],
      "meta": {},
      "schemas": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Group action reference](actions/create-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fileCloud/latest/actions/create-group).
