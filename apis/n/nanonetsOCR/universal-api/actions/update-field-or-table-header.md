# Nanonets OCR: Update Field Or Table Header



```
PUT https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/update-field-or-table-header
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nanonets OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/update-field-or-table-header" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowId": "string",
  "fieldId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/update-field-or-table-header', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowId": "string",
    "fieldId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflowId` | list | yes | Workflow ID that owns the field or table header. |
| `fieldId` | string | yes | Field or table header ID to update. |
| `name` | string | yes | Updated field or table header name using only alphanumeric characters and underscores. |

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

Through the native Nanonets OCR API, this operation is `PATCH /workflows/:workflow_id/fields/:field_id` (base URL `https://app.nanonets.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-field-or-table-header.md) for the provider-specific parameters and requirements.

