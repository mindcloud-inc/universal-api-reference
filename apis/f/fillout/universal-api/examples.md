# Fillout Universal API Examples

These examples use the MindCloud API key and Fillout connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Forms

Retrieves forms from Fillout.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fillout/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fillout/latest/actions/list-forms?${params}`, {
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
      "formId": "string",
      "id": 1,
      "isPublished": true,
      "name": "Ava Chen",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Forms action reference](actions/list-forms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fillout/latest/actions/list-forms).

## Create Database

Creates a new database in Fillout.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fillout/latest/actions/create-database" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "tables[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fillout/latest/actions/create-database', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "tables[]": [{}]
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
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "tables": [
        {}
      ],
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Database action reference](actions/create-database.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fillout/latest/actions/create-database).
