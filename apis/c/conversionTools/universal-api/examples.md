# Conversion Tools Universal API Examples

These examples use the MindCloud API key and Conversion Tools connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authenticated User Info

Retrieves authenticated user info from Conversion Tools.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/get-authenticated-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/get-authenticated-user-info?${params}`, {
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
      "email": "ava@example.com",
      "error": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Authenticated User Info action reference](actions/get-authenticated-user-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/conversionTools/latest/actions/get-authenticated-user-info).

## Create Conversion Task

Creates a new conversion task in Conversion Tools.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/create-conversion-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "convert.jpg_to_pdf",
  "options": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/conversionTools/latest/actions/create-conversion-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "convert.jpg_to_pdf",
    "options": "[object Object]"
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
      "error": "string",
      "message": "string",
      "sandbox": true,
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Conversion Task action reference](actions/create-conversion-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/conversionTools/latest/actions/create-conversion-task).
