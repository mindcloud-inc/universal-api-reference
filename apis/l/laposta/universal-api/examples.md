# Laposta Universal API Examples

These examples use the MindCloud API key and Laposta connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Lists

Retrieves lists from Laposta.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laposta/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/laposta/latest/actions/list-lists?${params}`, {
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
      "data": [
        {
          "list": {
            "listId": "string",
            "locked": true,
            "name": "Ava Chen",
            "state": "string"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Lists action reference](actions/list-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/laposta/latest/actions/list-lists).

## Create Field

Creates a custom field in Laposta.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/laposta/latest/actions/create-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "name": "Ava Chen",
  "datatype": "date",
  "required": true,
  "inForm": true,
  "inList": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laposta/latest/actions/create-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "name": "Ava Chen",
    "datatype": "date",
    "required": true,
    "inForm": true,
    "inList": true
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
      "field": {
        "datatype": "string",
        "defaultValue": "string",
        "fieldId": "string",
        "inForm": true,
        "inList": true,
        "listId": "string",
        "name": "Ava Chen",
        "required": true,
        "state": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Field action reference](actions/create-field.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/laposta/latest/actions/create-field).
