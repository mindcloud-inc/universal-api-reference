# Workiom Universal API Examples

These examples use the MindCloud API key and Workiom connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Apps

Retrieves apps from your Workiom workspace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workiom/latest/actions/list-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workiom/latest/actions/list-apps?${params}`, {
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
      "items": [
        {
          "creationTime": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "icon": "string",
          "iconUrl": "https://example.com",
          "id": "string",
          "isPublic": true,
          "lastModificationTime": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Apps action reference](actions/list-apps.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/workiom/latest/actions/list-apps).

## Create Field

Creates a new custom field in Workiom.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workiom/latest/actions/create-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workiom/latest/actions/create-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "allowMultiple": true,
      "dataType": "string",
      "defaultValue": "string",
      "description": "string",
      "id": "string",
      "isAssociation": true,
      "isComputed": true,
      "isPrimary": true,
      "isRequired": true,
      "isVisible": true,
      "linkedListId": "https://example.com",
      "linkedViewId": 1,
      "listId": "string",
      "name": "Ava Chen",
      "order": 1,
      "summaryType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Field action reference](actions/create-field.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/workiom/latest/actions/create-field).
