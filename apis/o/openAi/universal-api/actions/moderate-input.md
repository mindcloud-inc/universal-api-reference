# Open AI: Moderate Input

Moderates text or image inputs in Open AI.

```
POST https://connect.mindcloud.co/v1/universal/openAi/latest/actions/moderate-input
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/moderate-input" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openAi/latest/actions/moderate-input', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input` | string | yes | Input text to moderate. |
| `model` | list | no | Moderation model ID. Default: `omni-moderation-latest`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "model": "string",
      "results": [
        {
          "categories": {
            "harassment": true,
            "hate": true,
            "illicit": true,
            "selfHarm": true,
            "sexual": true,
            "violence": true
          },
          "categoryAppliedInputTypes": {
            "harassment": [
              "string"
            ],
            "hate": [
              "string"
            ],
            "illicit": [
              "string"
            ],
            "selfHarm": [
              "string"
            ],
            "sexual": [
              "string"
            ],
            "violence": [
              "string"
            ]
          },
          "categoryScores": {
            "harassment": 1,
            "hate": 1,
            "illicit": 1,
            "selfHarm": 1,
            "sexual": 1,
            "violence": 1
          },
          "flagged": true
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
| `id` | string |  |
| `model` | string |  |
| `results[].categories.harassment` | boolean |  |
| `results[].categories.hate` | boolean |  |
| `results[].categories.illicit` | boolean |  |
| `results[].categories.selfHarm` | boolean |  |
| `results[].categories.sexual` | boolean |  |
| `results[].categories.violence` | boolean |  |
| `results[].categoryAppliedInputTypes.harassment[]` | string |  |
| `results[].categoryAppliedInputTypes.hate[]` | string |  |
| `results[].categoryAppliedInputTypes.illicit[]` | string |  |
| `results[].categoryAppliedInputTypes.selfHarm[]` | string |  |
| `results[].categoryAppliedInputTypes.sexual[]` | string |  |
| `results[].categoryAppliedInputTypes.violence[]` | string |  |
| `results[].categoryScores.harassment` | number |  |
| `results[].categoryScores.hate` | number |  |
| `results[].categoryScores.illicit` | number |  |
| `results[].categoryScores.selfHarm` | number |  |
| `results[].categoryScores.sexual` | number |  |
| `results[].categoryScores.violence` | number |  |
| `results[].flagged` | boolean |  |

## Native endpoint

Through the native Open AI API, this operation is `POST v1/moderations` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/moderate-input.md) for the provider-specific parameters and requirements.

