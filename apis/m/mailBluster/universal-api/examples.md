# MailBluster Universal API Examples

These examples use the MindCloud API key and MailBluster connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Fields

Retrieves all custom fields from MailBluster.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/list-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/list-fields?${params}`, {
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
      "fields": [
        {
          "createdAt": "string",
          "fieldLabel": "string",
          "fieldMergeTag": "string",
          "id": 1,
          "updatedAt": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Fields action reference](actions/list-fields.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailBluster/latest/actions/list-fields).

## Create Lead

Creates a new lead in MailBluster.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "subscribed": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "subscribed": true
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
      "lead": {
        "createdAt": "string",
        "email": "ava@example.com",
        "fields": {},
        "firstName": "Ava",
        "fullName": "Ava Chen",
        "id": 1,
        "ipAddress": "string",
        "lastName": "Chen",
        "meta": {},
        "optInStatus": "string",
        "subscribed": true,
        "tags": [
          "string"
        ],
        "timezone": "string",
        "updatedAt": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Lead action reference](actions/create-lead.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailBluster/latest/actions/create-lead).
