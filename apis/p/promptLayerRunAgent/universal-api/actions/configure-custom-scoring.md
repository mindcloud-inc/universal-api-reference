# PromptLayer Run Agent: Configure Custom Scoring

Updates custom scoring for a PromptLayer evaluation.

```
PUT https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/configure-custom-scoring
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/configure-custom-scoring" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reportId": "45405",
  "column_names[]": "Human Rating 2 Updated"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/configure-custom-scoring', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reportId": "45405",
    "column_names[]": "Human Rating 2 Updated"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reportId` | number | yes | ID of the evaluation pipeline report. Example: `45405`. |
| `column_names[]` | array<string> | yes | List of column names to include in score calculation. Example: `Human Rating 2 Updated`. |
| `code` | string | no | Optional Python or JavaScript code for custom score calculation. Example: `scores = [row.get("Human Rating 2 Updated") for row in data if isinstance(row.get("Human Rating 2 Updated"), (int, float))]\nreturn {"score": (sum(scores) / len(scores) * 10) if scores else 0}`. |
| `codeLanguage` | string | no | Language of the custom code: PYTHON or JAVASCRIPT. Example: `PYTHON`. |

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

Through the native PromptLayer Run Agent API, this operation is `PATCH /reports/:reportId/score-card` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/configure-custom-scoring.md) for the provider-specific parameters and requirements.

