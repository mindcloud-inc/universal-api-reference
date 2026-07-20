# SurveyMethods: List Surveys



```
GET https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/list-surveys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveyMethods `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/list-surveys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/list-surveys?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "pages": [
        {
          "number": 1,
          "surveys": [
            {
              "closed_date": "2026-05-07T12:00:00.000Z",
              "code": "string",
              "created_date": "2026-05-07T12:00:00.000Z",
              "latest_launch_date": "2026-05-07T12:00:00.000Z",
              "status": "string",
              "title": "string",
              "web_launch_url": "https://example.com"
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
| `pages[].surveys` | array<object> |  |
| `pages[].surveys[].closed_date` | date |  |
| `pages[].surveys[].code` | string |  |
| `pages[].surveys[].created_date` | date |  |
| `pages[].surveys[].latest_launch_date` | date |  |
| `pages[].surveys[].status` | string |  |
| `pages[].surveys[].title` | string |  |
| `pages[].surveys[].web_launch_url` | string |  |
| `rowcount` | number |  |
| `status` | string |  |

## Native endpoint

Through the native SurveyMethods API, this operation is `GET /:loginId/:apiKey/surveys/details/` (base URL `https://api.surveymethods.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-surveys.md) for the provider-specific parameters and requirements.

