# snapADDY: Get Question Option



```
GET https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-question-option
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a snapADDY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-question-option?connectionId=$CONNECTION_ID&questionOptionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "questionOptionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-question-option?${params}`, {
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
| `questionOptionId` | string | yes | Question option identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "mappingId": "string",
      "questionId": "string",
      "questionOptionType": 1,
      "sequenceNumber": 1,
      "texts": {},
      "validation": {},
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `mappingId` | string |  |
| `questionId` | string |  |
| `questionOptionType` | number |  |
| `sequenceNumber` | number |  |
| `texts` | object |  |
| `validation` | object |  |
| `value` | string |  |

## Native endpoint

Through the native snapADDY API, this operation is `GET /visitreport/v1/questionOption/:questionOptionId` (base URL `https://api.snapaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-question-option.md) for the provider-specific parameters and requirements.

