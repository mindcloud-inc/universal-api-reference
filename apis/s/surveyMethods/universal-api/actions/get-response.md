# SurveyMethods: Get Response



```
GET https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/get-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveyMethods `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/get-response?connectionId=$CONNECTION_ID&surveyCode=string&responseCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyCode": "string",
  "responseCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/get-response?${params}`, {
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
| `surveyCode` | string | yes | SurveyMethods survey code. |
| `responseCode` | string | yes | SurveyMethods response code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "questions": [
        {
          "answer": [
            {
              "additional_comments": {
                "text": "string",
                "value": "string"
              },
              "value": "string"
            }
          ],
          "question_code": "string",
          "question_text": "string"
        }
      ],
      "rowcount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `questions` | array<object> |  |
| `questions[].answer` | array<object> |  |
| `questions[].answer[].additional_comments` | object |  |
| `questions[].answer[].additional_comments.text` | string |  |
| `questions[].answer[].additional_comments.value` | string |  |
| `questions[].answer[].value` | string |  |
| `questions[].question_code` | string |  |
| `questions[].question_text` | string |  |
| `rowcount` | number |  |
| `status` | string |  |

## Native endpoint

Through the native SurveyMethods API, this operation is `GET /:loginId/:apiKey/responses/:surveyCode/detail/:responseCode/` (base URL `https://api.surveymethods.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-response.md) for the provider-specific parameters and requirements.

