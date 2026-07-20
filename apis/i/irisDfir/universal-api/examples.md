# Iris Dfir Universal API Examples

These examples use the MindCloud API key and Iris Dfir connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Cases



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/list-cases?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/list-cases?${params}`, {
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
      "case_customer_id": 1,
      "case_description": "string",
      "case_id": 1,
      "case_name": "Ava Chen",
      "case_soc_id": "string",
      "case_uuid": "string",
      "close_date": "2026-05-07T12:00:00.000Z",
      "closing_note": "string",
      "custom_attributes": {},
      "modification_history": {},
      "open_date": "2026-05-07T12:00:00.000Z",
      "owner": {
        "id": 1,
        "user_email": "ava@example.com",
        "user_login": "string",
        "user_name": "Ava Chen"
      },
      "severity_id": 1,
      "state": {
        "protected": true,
        "state_description": "string",
        "state_id": 1,
        "state_name": "Ava Chen"
      },
      "status_id": 1,
      "user_id": 1
    }
  ],
  "meta": {}
}
```

See the full [List Cases action reference](actions/list-cases.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/irisDfir/latest/actions/list-cases).

## Add Note



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/add-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "directoryId": 1,
  "noteTitle": "string",
  "noteContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/add-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "directoryId": 1,
    "noteTitle": "string",
    "noteContent": "string"
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
      "data": {
        "comments": [
          {}
        ],
        "custom_attributes": {},
        "directory_id": 1,
        "directory": {
          "case_id": 1,
          "id": 1,
          "name": "Ava Chen",
          "parent_id": 1
        },
        "modification_history": {},
        "note_case_id": 1,
        "note_content": "string",
        "note_creationdate": "2026-05-07T12:00:00.000Z",
        "note_id": 1,
        "note_lastupdate": "2026-05-07T12:00:00.000Z",
        "note_title": "string",
        "note_user": 1,
        "note_uuid": "string"
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Note action reference](actions/add-note.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/irisDfir/latest/actions/add-note).
