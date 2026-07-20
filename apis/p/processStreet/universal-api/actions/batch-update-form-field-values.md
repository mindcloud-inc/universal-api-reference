# Process Street: Batch Update Form Field Values



```
PUT https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/batch-update-form-field-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Street `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/batch-update-form-field-values" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowRunId": "string",
  "fields[].id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/batch-update-form-field-values', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowRunId": "string",
    "fields[].id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflowRunId` | string | yes | The ID of the workflow run. |
| `fields[]` | array<object> | no | Form field values to update. |
| `fields[].id` | string | yes | The ID of the form field value to update. |
| `fields[].value` | string | no | Single value for the form field. |
| `fields[].values[]` | array<string> | no | Multiple values for the form field. |
| `fields[].timeHidden` | boolean | no | Whether to hide the time portion for date fields. |
| `fields[].dataSetRowId` | string | no | Optional data set row ID for linked dropdowns. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "fieldType": "string",
      "id": "string",
      "key": "string",
      "label": "string",
      "links": [
        {}
      ],
      "taskId": "string",
      "updatedBy": {},
      "updatedDate": "2026-05-07T12:00:00.000Z",
      "workflowRunId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `fieldType` | string |  |
| `id` | string |  |
| `key` | string |  |
| `label` | string |  |
| `links` | array<object> |  |
| `taskId` | string |  |
| `updatedBy` | object |  |
| `updatedDate` | date |  |
| `workflowRunId` | string |  |

## Native endpoint

Through the native Process Street API, this operation is `POST /workflow-runs/:workflowRunId/form-fields` (base URL `https://public-api.process.st/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-update-form-field-values.md) for the provider-specific parameters and requirements.

