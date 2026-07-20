# PreCallAI Universal API Examples

These examples use the MindCloud API key and PreCallAI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Assistants

Retrieves assistants from PreCallAI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-assistants?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-assistants?${params}`, {
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
      "data": {
        "ai_model_id": 1,
        "company_name": "Ava Chen",
        "goal": "string",
        "id": "string",
        "language": "string",
        "name": "Ava Chen",
        "type": "string",
        "voice_id": "string",
        "voice_name": "Ava Chen"
      },
      "message": "string",
      "status": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [List Assistants action reference](actions/list-assistants.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/preCallAI/latest/actions/list-assistants).

## Bulk Upload Segment Contacts

Bulk uploads segment contacts in PreCallAI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/bulk-upload-segment-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/bulk-upload-segment-contacts', {
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
      "data": {},
      "message": "string",
      "status": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Bulk Upload Segment Contacts action reference](actions/bulk-upload-segment-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/preCallAI/latest/actions/bulk-upload-segment-contacts).
