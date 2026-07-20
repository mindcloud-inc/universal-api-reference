# snapADDY: Get Answer



```
GET https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-answer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a snapADDY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-answer?connectionId=$CONNECTION_ID&answerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "answerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-answer?${params}`, {
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
| `answerId` | string | yes | Answer identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "participantId": "string",
      "questionId": "string"
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

## Native endpoint

Through the native snapADDY API, this operation is `GET /visitreport/v1/answer/:answerId` (base URL `https://api.snapaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-answer.md) for the provider-specific parameters and requirements.

