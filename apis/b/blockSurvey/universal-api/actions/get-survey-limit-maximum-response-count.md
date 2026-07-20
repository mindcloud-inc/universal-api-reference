# BlockSurvey: Get Survey Limit Maximum Response Count

Retrieves a survey response limit from BlockSurvey.

```
GET https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/get-survey-limit-maximum-response-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlockSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/get-survey-limit-maximum-response-count?connectionId=$CONNECTION_ID&surveyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/get-survey-limit-maximum-response-count?${params}`, {
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
| `surveyId` | string | yes | The ID of the survey. |
| `teamId` | string | no | The team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "limitMaximumResponseCount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limitMaximumResponseCount` | number |  |
| `status` | string |  |

## Native endpoint

Through the native BlockSurvey API, this operation is `GET /v1/survey/limit_maximum_response_count` (base URL `https://api3.blocksurvey.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey-limit-maximum-response-count.md) for the provider-specific parameters and requirements.

