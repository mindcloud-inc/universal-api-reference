# PromptLayer Run Agent: Add Column To Evaluation Pipeline

Adds a column to a PromptLayer evaluation pipeline.

```
PUT https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/add-column-to-evaluation-pipeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/add-column-to-evaluation-pipeline" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reportId": "45405",
  "columnType": "HUMAN",
  "name": "Human Rating 2",
  "configuration": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/add-column-to-evaluation-pipeline', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reportId": "45405",
    "columnType": "HUMAN",
    "name": "Human Rating 2",
    "configuration": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reportId` | number | yes | ID of the evaluation pipeline report. Example: `45405`. |
| `columnType` | string | yes | Type of evaluation column to add. Example: `HUMAN`. |
| `name` | string | yes | Display name for the column. Example: `Human Rating 2`. |
| `configuration` | object | yes | Column-type-specific configuration object. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `position` | number | no | Optional position for the column. Example: `8`. |
| `isPartOfScore` | boolean | no | Whether to include this column in default score calculation. Example: `false`. |

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

Through the native PromptLayer Run Agent API, this operation is `POST /report-columns` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-column-to-evaluation-pipeline.md) for the provider-specific parameters and requirements.

