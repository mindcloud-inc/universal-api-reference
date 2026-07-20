# Softr Universal API Examples

These examples use the MindCloud API key and Softr connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Databases



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/softr/latest/actions/list-databases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/softr/latest/actions/list-databases?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "tablesCount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Databases action reference](actions/list-databases.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/softr/latest/actions/list-databases).

## Add Table Field



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/softr/latest/actions/add-table-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "tableId": "string",
  "name": "Ava Chen",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/softr/latest/actions/add-table-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "tableId": "string",
    "name": "Ava Chen",
    "type": "string"
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
      "aiOptions": {
        "aiFillable": true,
        "aiModel": "string",
        "aiOnly": true,
        "allowWebSearch": true,
        "canBeTriggeredManually": true,
        "prompt": "string",
        "runOnUpdateMode": "string",
        "runWhenRecordIsCreated": true,
        "runWhenRecordIsUpdated": true,
        "skipIfValueExists": true
      },
      "allowMultipleEntries": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "locked": true,
      "name": "Ava Chen",
      "options": {
        "maxLength": 1,
        "minLength": 1
      },
      "readonly": true,
      "required": true,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Table Field action reference](actions/add-table-field.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/softr/latest/actions/add-table-field).
