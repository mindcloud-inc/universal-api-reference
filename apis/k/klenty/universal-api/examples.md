# Klenty Universal API Examples

These examples use the MindCloud API key and Klenty connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Lists

Retrieves lists from Klenty.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klenty/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klenty/latest/actions/list-lists?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Lists action reference](actions/list-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/klenty/latest/actions/list-lists).

## Add Prospect Custom Field Value

Adds a custom field value to a prospect in Klenty.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/klenty/latest/actions/add-prospect-custom-field-value" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "customFields": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/klenty/latest/actions/add-prospect-custom-field-value', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "customFields": {}
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
      "details": {
        "email": "ava@example.com",
        "id": "string",
        "prospectOwner": "string",
        "source": "string",
        "status": true
      },
      "status": true
    }
  ],
  "meta": {}
}
```

See the full [Add Prospect Custom Field Value action reference](actions/add-prospect-custom-field-value.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/klenty/latest/actions/add-prospect-custom-field-value).
