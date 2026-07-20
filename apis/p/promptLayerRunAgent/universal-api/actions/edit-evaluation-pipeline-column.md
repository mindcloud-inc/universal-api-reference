# PromptLayer Run Agent: Edit Evaluation Pipeline Column

Updates a column in a PromptLayer evaluation pipeline.

```
PUT https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/edit-evaluation-pipeline-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/edit-evaluation-pipeline-column" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reportColumnId": "673853",
  "reportId": "45405",
  "columnType": "HUMAN",
  "name": "Human Rating 2 Updated",
  "configuration": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/edit-evaluation-pipeline-column', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reportColumnId": "673853",
    "reportId": "45405",
    "columnType": "HUMAN",
    "name": "Human Rating 2 Updated",
    "configuration": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reportColumnId` | number | yes | ID of the report column to edit. Example: `673853`. |
| `reportId` | number | yes | ID of the evaluation pipeline report. Example: `45405`. |
| `columnType` | string | yes | Column type for the existing column. Example: `HUMAN`. |
| `name` | string | yes | Updated display name for the column. Example: `Human Rating 2 Updated`. |
| `configuration` | object | yes | Updated column configuration. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isPartOfScore` | boolean | no | Whether the column should count toward the default score. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "report_column": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `report_column` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `PATCH /report-columns/:reportColumnId` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-evaluation-pipeline-column.md) for the provider-specific parameters and requirements.

