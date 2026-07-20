# PromptLayer Run Agent: Create Evaluation Pipeline

Creates a new evaluation pipeline in PromptLayer.

```
POST https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-evaluation-pipeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-evaluation-pipeline" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datasetGroupId": "20196"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/create-evaluation-pipeline', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datasetGroupId": "20196"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasetGroupId` | number | yes | ID of the dataset group to use. Example: `20196`. |
| `name` | string | no | Name for the pipeline. If omitted, PromptLayer auto-generates one. Example: `MindCloud Stage 3 Eval Pipeline`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasetVersionNumber` | number | no | Specific dataset version to use. Uses latest if omitted. Example: `1`. |

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

Through the native PromptLayer Run Agent API, this operation is `POST /reports` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-evaluation-pipeline.md) for the provider-specific parameters and requirements.

