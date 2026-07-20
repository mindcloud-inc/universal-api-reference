# snapADDY: Get Question



```
GET https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a snapADDY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-question?connectionId=$CONNECTION_ID&questionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "questionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapADDY/latest/actions/get-question?${params}`, {
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
| `questionId` | string | yes | Question identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "column": 1,
      "groupId": "string",
      "id": "string",
      "mappingId": "string",
      "questionType": 1,
      "sequenceNumber": 1,
      "settings": {},
      "texts": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `column` | number |  |
| `groupId` | string |  |
| `id` | string |  |
| `mappingId` | string |  |
| `questionType` | number |  |
| `sequenceNumber` | number |  |
| `settings` | object |  |
| `texts` | object |  |

## Native endpoint

Through the native snapADDY API, this operation is `GET /visitreport/v1/question/:questionId` (base URL `https://api.snapaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-question.md) for the provider-specific parameters and requirements.

