# SatisMeter: Get Survey Statistics



```
GET https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/get-survey-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SatisMeter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/get-survey-statistics?connectionId=$CONNECTION_ID&campaignId=61fce0adea447e24ec27d609&projectId=61fce0adea447e24ec27d606" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "61fce0adea447e24ec27d609",
  "projectId": "61fce0adea447e24ec27d606"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/get-survey-statistics?${params}`, {
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
| `campaignId` | string | yes | Survey ID. Example: `61fce0adea447e24ec27d609`. |
| `endDate` | date | no | Filter statistics using responses recorded before this ISO 8601 timestamp. Example: `2026-03-17T23:59:59Z`. |
| `projectId` | string | yes | Project ID. Example: `61fce0adea447e24ec27d606`. |
| `startDate` | date | no | Filter statistics using responses recorded after this ISO 8601 timestamp. Example: `2026-03-01T00:00:00Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "questions": [
        {
          "id": "string",
          "label": "string",
          "statistics": {
            "answers": 1,
            "metric": {
              "type": "string",
              "value": 1
            },
            "values": [
              {
                "answers": 1,
                "value": 1
              }
            ]
          },
          "type": "string"
        }
      ],
      "statistics": {
        "displays": 1,
        "responseRate": 1,
        "responses": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `questions` | array<object> | Survey questions and per-question statistics. |
| `questions[].id` | string | Question ID. |
| `questions[].label` | string | Question label. |
| `questions[].statistics` | object | Question-level statistics. |
| `questions[].statistics.answers` | number | Number of answers for the question. |
| `questions[].statistics.metric` | object | Question metric summary when provided. |
| `questions[].statistics.metric.type` | string | Metric type. |
| `questions[].statistics.metric.value` | number | Metric value. |
| `questions[].statistics.values` | array<object> | Per-scale answer counts when provided. |
| `questions[].statistics.values[].answers` | number | Answer count for the scale value. |
| `questions[].statistics.values[].value` | number | Scale value. |
| `questions[].type` | string | Question type. |
| `statistics` | object | Survey response totals. |
| `statistics.displays` | number | Total survey displays. |
| `statistics.responseRate` | number | Survey response rate. |
| `statistics.responses` | number | Total survey responses. |

## Native endpoint

Through the native SatisMeter API, this operation is `GET /api/v3/projects/:projectId/campaigns/:campaignId/statistics` (base URL `https://app.satismeter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey-statistics.md) for the provider-specific parameters and requirements.

