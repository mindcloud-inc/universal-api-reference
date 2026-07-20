# PromptLayer Run Agent: Rename Evaluation Pipeline

Renames a PromptLayer evaluation pipeline.

```
PUT https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/rename-evaluation-pipeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/rename-evaluation-pipeline" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reportId": "45403",
  "name": "MindCloud Stage 3 Eval Pipeline Renamed Again"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/rename-evaluation-pipeline', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reportId": "45403",
    "name": "MindCloud Stage 3 Eval Pipeline Renamed Again"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reportId` | number | yes | ID of the evaluation pipeline report to rename. Example: `45403`. |
| `name` | string | yes | New name for the evaluation pipeline. Example: `MindCloud Stage 3 Eval Pipeline Renamed Again`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "report": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `report` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `PATCH /reports/:reportId/rename` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-evaluation-pipeline.md) for the provider-specific parameters and requirements.

