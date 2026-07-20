# PromptLayer Run Agent: Get Evaluation Score

Retrieves the score for a PromptLayer evaluation.

```
GET https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-evaluation-score
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-evaluation-score?connectionId=$CONNECTION_ID&reportId=45406" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reportId": "45406"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-evaluation-score?${params}`, {
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
| `reportId` | number | yes | ID of the evaluation report to retrieve score details for. Example: `45406`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "score": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `score` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `GET /reports/:reportId/score` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-evaluation-score.md) for the provider-specific parameters and requirements.

