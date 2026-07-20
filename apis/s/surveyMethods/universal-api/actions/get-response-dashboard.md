# SurveyMethods: Get Response Dashboard



```
GET https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/get-response-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveyMethods `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/get-response-dashboard?connectionId=$CONNECTION_ID&surveyCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/get-response-dashboard?${params}`, {
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
      "rowcount": 1,
      "status": "string",
      "survey": {
        "response": {
          "all": {
            "completed": 1,
            "partial": 1,
            "total": 1
          },
          "email": {
            "completed": 1,
            "invited": 1,
            "opted_out": 1,
            "partial": 1,
            "total": 1
          },
          "points_summary": {
            "average": {
              "percentage": "string",
              "value": "string"
            },
            "highest": {
              "percentage": "string",
              "value": "string"
            },
            "lowest": {
              "percentage": "string",
              "value": "string"
            },
            "max_attainable": {
              "percentage": "string",
              "value": "string"
            },
            "median": {
              "percentage": "string",
              "value": "string"
            }
          },
          "web": {
            "completed": 1,
            "partial": 1,
            "total": 1
          }
        },
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rowcount` | number |  |
| `status` | string |  |
| `survey` | object |  |
| `survey.response` | object |  |
| `survey.response.all` | object |  |
| `survey.response.all.completed` | number |  |
| `survey.response.all.partial` | number |  |
| `survey.response.all.total` | number |  |
| `survey.response.email` | object |  |
| `survey.response.email.completed` | number |  |
| `survey.response.email.invited` | number |  |
| `survey.response.email.opted_out` | number |  |
| `survey.response.email.partial` | number |  |
| `survey.response.email.total` | number |  |
| `survey.response.points_summary` | object |  |
| `survey.response.points_summary.average.percentage` | string |  |
| `survey.response.points_summary.average.value` | string |  |
| `survey.response.points_summary.highest.percentage` | string |  |
| `survey.response.points_summary.highest.value` | string |  |
| `survey.response.points_summary.lowest.percentage` | string |  |
| `survey.response.points_summary.lowest.value` | string |  |
| `survey.response.points_summary.max_attainable.percentage` | string |  |
| `survey.response.points_summary.max_attainable.value` | string |  |
| `survey.response.points_summary.median.percentage` | string |  |
| `survey.response.points_summary.median.value` | string |  |
| `survey.response.web` | object |  |
| `survey.response.web.completed` | number |  |
| `survey.response.web.partial` | number |  |
| `survey.response.web.total` | number |  |
| `survey.title` | string |  |

## Native endpoint

Through the native SurveyMethods API, this operation is `GET /:loginId/:apiKey/responses/:surveyCode/dashboard/` (base URL `https://api.surveymethods.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-response-dashboard.md) for the provider-specific parameters and requirements.

