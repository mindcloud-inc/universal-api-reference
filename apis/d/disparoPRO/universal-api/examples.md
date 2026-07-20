# Disparo PRO Universal API Examples

These examples use the MindCloud API key and Disparo PRO connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Templates

Retrieves templates from Disparo PRO.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/list-templates?${params}`, {
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
      "category": "string",
      "contentType": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "language": "string",
      "name": "Ava Chen",
      "rejectionReason": "string",
      "reviewStatus": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "variables": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Templates action reference](actions/list-templates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/disparoPRO/latest/actions/list-templates).

## Activate Template

Updates a template to active in Disparo PRO.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/activate-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/disparoPRO/latest/actions/activate-template', {
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
      "category": "string",
      "contentType": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "language": "string",
      "name": "Ava Chen",
      "rejectionReason": "string",
      "reviewStatus": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "variables": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Activate Template action reference](actions/activate-template.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/disparoPRO/latest/actions/activate-template).
