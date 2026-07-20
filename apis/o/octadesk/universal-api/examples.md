# Octadesk Universal API Examples

These examples use the MindCloud API key and Octadesk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check API Key

Checks whether an Octadesk API key is valid.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/check-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/check-api-key?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Check API Key action reference](actions/check-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/octadesk/latest/actions/check-api-key).

## Create Contact

Creates a contact in Octadesk.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "codex.octadesk.test@example.com",
  "name": "Codex Test Contact"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "codex.octadesk.test@example.com",
    "name": "Codex Test Contact"
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
      "customFields": [
        "string"
      ],
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "organization": {
        "description": "string",
        "domains": [
          "string"
        ],
        "id": "string",
        "name": "Ava Chen"
      },
      "phoneContacts": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/octadesk/latest/actions/create-contact).
