# Print Autopilot Universal API Examples

These examples use the MindCloud API key and Print Autopilot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Print Jobs

Retrieves print jobs from Print Autopilot.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printAutopilot/latest/actions/list-print-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printAutopilot/latest/actions/list-print-jobs?${params}`, {
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
      "documents": [
        {
          "base64": "string",
          "file_name": "Ava Chen",
          "id": 1,
          "printable_queue_id": 1
        }
      ],
      "PaperSize": {
        "height": 1,
        "id": 1,
        "name": "Ava Chen",
        "rawKind": "string",
        "width": 1
      },
      "Printer": {
        "id": 1,
        "name": "Ava Chen"
      },
      "scaling": 1
    }
  ],
  "meta": {}
}
```

See the full [List Print Jobs action reference](actions/list-print-jobs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/printAutopilot/latest/actions/list-print-jobs).

## Create Document

Creates a document in Print Autopilot from a base64 PDF.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/printAutopilot/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "base64": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printAutopilot/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "base64": "string"
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Document action reference](actions/create-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/printAutopilot/latest/actions/create-document).
