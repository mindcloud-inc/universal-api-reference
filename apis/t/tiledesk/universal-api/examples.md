# Tiledesk Universal API Examples

These examples use the MindCloud API key and Tiledesk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Project Details

Retrieves details for the current project from Tiledesk.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/get-project-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/get-project-details?${params}`, {
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
      "_id": "string",
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Project Details action reference](actions/get-project-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tiledesk/latest/actions/get-project-details).

## Close Request

Closes a request in the current Tiledesk project.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/close-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requestId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tiledesk/latest/actions/close-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requestId": "string"
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
      "_id": "string",
      "closed_at": "string",
      "request_id": "string",
      "status": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Close Request action reference](actions/close-request.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tiledesk/latest/actions/close-request).
