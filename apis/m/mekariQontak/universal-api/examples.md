# Mekari Qontak Universal API Examples

These examples use the MindCloud API key and Mekari Qontak connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Contact Fields

Retrieves contact fields from Mekari Qontak.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mekariQontak/latest/actions/get-contact-template?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mekariQontak/latest/actions/get-contact-template?${params}`, {
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
      "meta": {
        "developerMessage": "string",
        "errorCode": "string",
        "info": "string",
        "message": "string",
        "status": 1,
        "type": "string"
      },
      "response": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Contact Fields action reference](actions/get-contact-template.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mekariQontak/latest/actions/get-contact-template).

## Create Task Category

Creates a task category in Mekari Qontak.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mekariQontak/latest/actions/add-task-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mekariQontak/latest/actions/add-task-category', {
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
      "meta": {
        "developerMessage": "string",
        "errorCode": "string",
        "info": "string",
        "message": "string",
        "status": 1,
        "type": "string"
      },
      "response": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Task Category action reference](actions/add-task-category.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mekariQontak/latest/actions/add-task-category).
