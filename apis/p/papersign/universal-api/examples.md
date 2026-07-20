# Papersign Universal API Examples

These examples use the MindCloud API key and Papersign connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Papersign Spaces



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/papersign/latest/actions/list-papersign-spaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/papersign/latest/actions/list-papersign-spaces?${params}`, {
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
      "has_more": true,
      "limit": 1,
      "results": {
        "spaces": [
          {
            "allow_team_access": true,
            "id": 1,
            "name": "Ava Chen",
            "root_folder_id": 1
          }
        ]
      },
      "skip": 1,
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [List Papersign Spaces action reference](actions/list-papersign-spaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/papersign/latest/actions/list-papersign-spaces).

## Cancel Papersign Document



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/papersign/latest/actions/cancel-papersign-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/papersign/latest/actions/cancel-papersign-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "results": {
        "document": {
          "completed_at_utc": "2026-05-07T12:00:00.000Z",
          "created_at_utc": "2026-05-07T12:00:00.000Z",
          "folder": {
            "id": 1,
            "name": "Ava Chen",
            "space_id": 1
          },
          "id": "string",
          "name": "Ava Chen",
          "sent_at_utc": "2026-05-07T12:00:00.000Z",
          "space": {
            "id": 1,
            "name": "Ava Chen"
          },
          "status": "string",
          "updated_at_utc": "2026-05-07T12:00:00.000Z"
        }
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Papersign Document action reference](actions/cancel-papersign-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/papersign/latest/actions/cancel-papersign-document).
