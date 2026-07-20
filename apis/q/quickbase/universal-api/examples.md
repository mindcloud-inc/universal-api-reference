# Quickbase Universal API Examples

These examples use the MindCloud API key and Quickbase connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get App

Retrieves a Quickbase app by ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/get-app?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/get-app?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "dateFormat": "string",
      "description": "string",
      "hasEveryoneOnTheInternet": true,
      "id": "string",
      "memoryInfo": {},
      "name": "Ava Chen",
      "securityProperties": {},
      "timeZone": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get App action reference](actions/get-app.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quickbase/latest/actions/get-app).

## Create a Field

Creates a new field in Quickbase.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/create-a-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableId": "string",
  "label": "string",
  "fieldType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/create-a-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableId": "string",
    "label": "string",
    "fieldType": "string"
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
      "appearsByDefault": true,
      "audited": true,
      "fieldHelp": "string",
      "fieldType": "string",
      "findEnabled": true,
      "id": 1,
      "label": "string",
      "mode": "string",
      "permissions": [
        {}
      ],
      "properties": {},
      "required": true
    }
  ],
  "meta": {}
}
```

See the full [Create a Field action reference](actions/create-a-field.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quickbase/latest/actions/create-a-field).
