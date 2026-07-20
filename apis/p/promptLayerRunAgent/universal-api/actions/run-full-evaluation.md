# PromptLayer Run Agent: Run Full Evaluation

Runs a full evaluation in PromptLayer.

```
POST https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/run-full-evaluation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/run-full-evaluation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reportId": "45405",
  "name": "MindCloud Stage 3 Eval Run"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/run-full-evaluation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reportId": "45405",
    "name": "MindCloud Stage 3 Eval Run"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reportId` | number | yes | ID of the evaluation pipeline report to run. Example: `45405`. |
| `name` | string | yes | Name of the final report to be created. Example: `MindCloud Stage 3 Eval Run`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasetId` | number | no | Dataset ID to use for the report. If omitted, uses the pipeline default dataset. Example: `32101`. |
| `refreshDataset` | boolean | no | Whether to refresh the dataset before running the report. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "report_id": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `report_id` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `POST /reports/:reportId/run` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-full-evaluation.md) for the provider-specific parameters and requirements.

