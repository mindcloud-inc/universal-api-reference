# SurveyMethods: List Response Codes



```
GET https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/list-response-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveyMethods `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/list-response-codes?connectionId=$CONNECTION_ID&surveyCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/list-response-codes?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "pages": [
        {
          "number": 1,
          "responses": [
            {
              "code": "string",
              "email": "ava@example.com",
              "source": "string"
            }
          ]
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
| `pages` | array<object> |  |
| `pages[].number` | number |  |
| `pages[].responses` | array<object> |  |
| `pages[].responses[].code` | string |  |
| `pages[].responses[].email` | string |  |
| `pages[].responses[].source` | string |  |
| `rowcount` | number |  |
| `status` | string |  |

## Native endpoint

Through the native SurveyMethods API, this operation is `GET /:loginId/:apiKey/responses/:surveyCode/codes/` (base URL `https://api.surveymethods.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-response-codes.md) for the provider-specific parameters and requirements.

