# Shotstack Universal API Examples

These examples use the MindCloud API key and Shotstack connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Templates



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/list-templates?${params}`, {
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
      "message": "string",
      "response": {
        "owner": "string",
        "templates": [
          {}
        ]
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [List Templates action reference](actions/list-templates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shotstack/latest/actions/list-templates).

## Create Template



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {}
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
      "message": "string",
      "response": {
        "id": "string",
        "message": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Template action reference](actions/create-template.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shotstack/latest/actions/create-template).
