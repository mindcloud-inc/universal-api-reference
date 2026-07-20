# snapADDY: Get Answer Option



```
GET https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-answer-option
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a snapADDY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-answer-option?connectionId=$CONNECTION_ID&answerOptionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "answerOptionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-answer-option?${params}`, {
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
| `answerOptionId` | string | yes | Answer option identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "participantId": "string",
      "questionId": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `participantId` | string |  |
| `questionId` | string |  |
| `text` | string |  |

## Native endpoint

Through the native snapADDY API, this operation is `GET /visitreport/v1/answerOption/:answerOptionId` (base URL `https://api.snapaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-answer-option.md) for the provider-specific parameters and requirements.

