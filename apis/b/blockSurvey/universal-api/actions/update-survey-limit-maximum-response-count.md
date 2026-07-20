# BlockSurvey: Update Survey Limit Maximum Response Count

Updates a survey response limit in BlockSurvey.

```
PUT https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/update-survey-limit-maximum-response-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlockSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/update-survey-limit-maximum-response-count" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": "string",
  "limitMaximumResponseCountFlag": true,
  "limitMaximumResponseCount": 1,
  "teamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blockSurvey/latest/actions/update-survey-limit-maximum-response-count', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": "string",
    "limitMaximumResponseCountFlag": true,
    "limitMaximumResponseCount": 1,
    "teamId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | string | yes | The ID of the survey. |
| `limitMaximumResponseCountFlag` | boolean | yes | Flag to set the maximum response count. |
| `limitMaximumResponseCount` | number | yes | The maximum response count. |
| `teamId` | string | yes | The team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native BlockSurvey API, this operation is `POST /v1/survey/limit_maximum_response_count` (base URL `https://api3.blocksurvey.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-survey-limit-maximum-response-count.md) for the provider-specific parameters and requirements.

