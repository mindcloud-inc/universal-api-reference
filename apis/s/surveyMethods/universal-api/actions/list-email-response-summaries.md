# SurveyMethods: List Email Response Summaries



```
GET https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/list-email-response-summaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveyMethods `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/list-email-response-summaries?connectionId=$CONNECTION_ID&surveyCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/list-email-response-summaries?${params}`, {
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
      "custom_field_labels": {
        "label1": "string",
        "label2": "string",
        "label3": "string",
        "label4": "string",
        "label5": "string"
      },
      "pages": [
        {
          "number": 1,
          "responses": [
            {
              "code": "string",
              "custom_field_values": {
                "value1": "string",
                "value2": "string",
                "value3": "string",
                "value4": "string",
                "value5": "string"
              },
              "date_started": "2026-05-07T12:00:00.000Z",
              "duration": "string",
              "email": "ava@example.com",
              "ip_address": "string",
              "source": "string",
              "time_started": "string"
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
| `custom_field_labels` | object |  |
| `custom_field_labels.label1` | string |  |
| `custom_field_labels.label2` | string |  |
| `custom_field_labels.label3` | string |  |
| `custom_field_labels.label4` | string |  |
| `custom_field_labels.label5` | string |  |
| `pages` | array<object> |  |
| `pages[].number` | number |  |
| `pages[].responses` | array<object> |  |
| `pages[].responses[].code` | string |  |
| `pages[].responses[].custom_field_values` | object |  |
| `pages[].responses[].custom_field_values.value1` | string |  |
| `pages[].responses[].custom_field_values.value2` | string |  |
| `pages[].responses[].custom_field_values.value3` | string |  |
| `pages[].responses[].custom_field_values.value4` | string |  |
| `pages[].responses[].custom_field_values.value5` | string |  |
| `pages[].responses[].date_started` | date |  |
| `pages[].responses[].duration` | string |  |
| `pages[].responses[].email` | string |  |
| `pages[].responses[].ip_address` | string |  |
| `pages[].responses[].source` | string |  |
| `pages[].responses[].time_started` | string |  |
| `rowcount` | number |  |
| `status` | string |  |

## Native endpoint

Through the native SurveyMethods API, this operation is `GET /:loginId/:apiKey/responses/:surveyCode/summary/email/` (base URL `https://api.surveymethods.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-email-response-summaries.md) for the provider-specific parameters and requirements.

