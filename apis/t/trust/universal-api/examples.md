# Trust Universal API Examples

These examples use the MindCloud API key and Trust connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces

Retrieves workspaces from Trust.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trust/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trust/latest/actions/list-workspaces?${params}`, {
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
      "registeredWorkspaces": [
        "string"
      ],
      "workspaceDetails": [
        {
          "name": "Ava Chen",
          "website": "string",
          "workspaceId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trust/latest/actions/list-workspaces).

## Assign Testimonial To Widget

Assigns a testimonial to a Trust widget.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trust/latest/actions/assign-testimonial-to-widget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "widgetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trust/latest/actions/assign-testimonial-to-widget', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "widgetId": "string"
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
      "id": "string",
      "widgetId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Assign Testimonial To Widget action reference](actions/assign-testimonial-to-widget.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trust/latest/actions/assign-testimonial-to-widget).
