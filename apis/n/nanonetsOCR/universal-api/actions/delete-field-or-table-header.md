# Nanonets OCR: Delete Field Or Table Header



```
DELETE https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/delete-field-or-table-header
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nanonets OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/delete-field-or-table-header?connectionId=$CONNECTION_ID&workflowId=string&fieldId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string",
  "fieldId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/delete-field-or-table-header?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflowId` | list | yes | Workflow ID that owns the field or table header. |
| `fieldId` | string | yes | Field or table header ID to delete. |

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

Through the native Nanonets OCR API, this operation is `DELETE /workflows/:workflow_id/fields/:field_id` (base URL `https://app.nanonets.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-field-or-table-header.md) for the provider-specific parameters and requirements.

