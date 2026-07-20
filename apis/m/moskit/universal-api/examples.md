# Moskit Universal API Examples

These examples use the MindCloud API key and Moskit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves users from Moskit.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moskit/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moskit/latest/actions/list-users?${params}`, {
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
      "active": true,
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "jobTitle": "string",
      "levelBulk": true,
      "levelConfig": true,
      "levelDelete": true,
      "levelEdit": "string",
      "levelExport": true,
      "levelView": "string",
      "name": "Ava Chen",
      "phones": [
        [
          {}
        ]
      ],
      "picture": "string",
      "primaryPhone": {
        "id": 1
      },
      "team": {
        "id": 1
      },
      "timezone": {
        "id": 1
      },
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moskit/latest/actions/list-users).

## Create Activity

Creates a new activity in Moskit.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moskit/latest/actions/create-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "createdBy.id": 1,
  "responsible.id": 1,
  "dueDate": "2026-05-07T12:00:00.000Z",
  "type.id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moskit/latest/actions/create-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "createdBy.id": 1,
    "responsible.id": 1,
    "dueDate": "2026-05-07T12:00:00.000Z",
    "type.id": 1
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
      "companies": [
        [
          {}
        ]
      ],
      "contacts": [
        [
          {}
        ]
      ],
      "createdBy": {
        "id": 1
      },
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "deals": [
        [
          {}
        ]
      ],
      "doneDate": "2026-05-07T12:00:00.000Z",
      "doneNotes": "string",
      "doneSource": "string",
      "doneUser": {
        "id": 1
      },
      "dueDate": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "entityCustomFields": [
        [
          {}
        ]
      ],
      "firstTry": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "lastTry": "2026-05-07T12:00:00.000Z",
      "notes": "string",
      "origin": "string",
      "projects": [
        [
          {}
        ]
      ],
      "responsible": {
        "id": 1
      },
      "source": "string",
      "title": "string",
      "totalDays": 1,
      "totalTries": 1,
      "type": {
        "id": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Activity action reference](actions/create-activity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moskit/latest/actions/create-activity).
