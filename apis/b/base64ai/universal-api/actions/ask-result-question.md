# Base64.ai: Ask Result Question

Retrieves answers to questions about a Base64.ai result.

```
GET https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/ask-result-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Base64.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/ask-result-question?connectionId=$CONNECTION_ID&resultUuid=string&questions%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resultUuid": "string",
  "questions[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/ask-result-question?${params}`, {
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
| `resultUuid` | string | yes | Base64.ai result UUID. |
| `questions[]` | array<string> | yes | One or more natural-language questions about the result. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "locale": "string",
      "location": {
        "bottomLeft": {
          "x": 1,
          "y": 1
        },
        "bottomRight": {
          "x": 1,
          "y": 1
        },
        "pageNumber": 1,
        "source": {
          "resultUUID": "string",
          "type": "string"
        },
        "topLeft": {
          "x": 1,
          "y": 1
        },
        "topRight": {
          "x": 1,
          "y": 1
        }
      },
      "modality": "string",
      "suggestedQuestions": [
        "string"
      ],
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `locale` | string |  |
| `location.bottomLeft.x` | number |  |
| `location.bottomLeft.y` | number |  |
| `location.bottomRight.x` | number |  |
| `location.bottomRight.y` | number |  |
| `location.pageNumber` | number |  |
| `location.source.resultUUID` | string |  |
| `location.source.type` | string |  |
| `location.topLeft.x` | number |  |
| `location.topLeft.y` | number |  |
| `location.topRight.x` | number |  |
| `location.topRight.y` | number |  |
| `modality` | string |  |
| `suggestedQuestions[]` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Base64.ai API, this operation is `POST /api/result/ask/:resultUuid` (base URL `https://base64.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ask-result-question.md) for the provider-specific parameters and requirements.

