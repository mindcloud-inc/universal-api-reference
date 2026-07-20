# Favro Universal API Examples

These examples use the MindCloud API key and Favro connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Organizations

Retrieves organizations from Favro.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/favro/latest/actions/get-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/favro/latest/actions/get-organizations?${params}`, {
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
      "name": "Ava Chen",
      "organizationId": "string",
      "sharedToUsers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Organizations action reference](actions/get-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/favro/latest/actions/get-organizations).

## Create Card

Creates a new card in Favro.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/favro/latest/actions/create-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "columnId": "string",
  "name": "Ava Chen",
  "widgetCommonId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/favro/latest/actions/create-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "columnId": "string",
    "name": "Ava Chen",
    "widgetCommonId": "string"
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
      "archived": true,
      "assignments": [
        "string"
      ],
      "attachments": [
        "string"
      ],
      "cardCommonId": "string",
      "cardId": "string",
      "columnId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdByUserId": "string",
      "customFields": [
        {}
      ],
      "dependencies": [
        "string"
      ],
      "favroAttachments": [
        "string"
      ],
      "isLane": true,
      "listPosition": 1,
      "name": "Ava Chen",
      "organizationId": "string",
      "position": 1,
      "sequentialId": 1,
      "sheetPosition": 1,
      "tags": [
        "string"
      ],
      "tasksDone": 1,
      "tasksTotal": 1,
      "timeOnBoard": {},
      "timeOnColumns": {},
      "widgetCommonId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Card action reference](actions/create-card.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/favro/latest/actions/create-card).
