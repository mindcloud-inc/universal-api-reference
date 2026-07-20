# Nanonets OCR: Set Fields And Table Headers



```
PUT https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/set-fields-and-table-headers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nanonets OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/set-fields-and-table-headers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowId": "Select a workflow",
  "fields[]": "[object Object],[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/set-fields-and-table-headers', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowId": "Select a workflow",
    "fields[]": "[object Object],[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflowId` | list | yes | Workflow identifier. Example: `Select a workflow`. |
| `fields[]` | array<object> | yes | Array of field objects with name values. Example: `[object Object],[object Object]`. |
| `table_headers[]` | array<object> | no | Array of table header objects with name values. Example: `[object Object],[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "description": "string",
      "fields": [
        {
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "id": "string",
      "settings": {
        "tableCapture": true
      },
      "tableHeaders": [
        {
          "id": "string",
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `description` | string |  |
| `fields[].id` | string |  |
| `fields[].name` | string |  |
| `id` | string |  |
| `settings.tableCapture` | boolean |  |
| `tableHeaders[].id` | string |  |
| `tableHeaders[].name` | string |  |

## Native endpoint

Through the native Nanonets OCR API, this operation is `PUT /workflows/:workflow_id/fields` (base URL `https://app.nanonets.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-fields-and-table-headers.md) for the provider-specific parameters and requirements.

