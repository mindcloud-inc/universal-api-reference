# Nanonets OCR Universal API Examples

These examples use the MindCloud API key and Nanonets OCR connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Available Workflow Types



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/list-available-workflow-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/list-available-workflow-types?${params}`, {
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
      "workflowTypes": [
        {
          "description": "string",
          "id": "string",
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Available Workflow Types action reference](actions/list-available-workflow-types.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nanonetsOCR/latest/actions/list-available-workflow-types).

## Create Workflow



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/create-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/create-workflow', {
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
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "settings": {
        "tableCapture": true
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Workflow action reference](actions/create-workflow.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nanonetsOCR/latest/actions/create-workflow).
