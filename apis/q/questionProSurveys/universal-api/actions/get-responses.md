# QuestionPro Surveys: Get Responses



```
GET https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuestionPro Surveys `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-responses?connectionId=$CONNECTION_ID&limit=25&offset=0&surveyId=1234567" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "surveyId": "1234567"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-responses?${params}`, {
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
| `surveyId` | number | yes | The QuestionPro survey ID. Example: `1234567`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browser": "string",
      "currentInset": "string",
      "customVariables": {},
      "dataQuality": "string",
      "dataQualityScore": 1,
      "duplicate": true,
      "externalReference": "string",
      "language": "string",
      "location": {},
      "operatingSystem": "string",
      "osDeviceType": "string",
      "responseID": 1,
      "responseSet": [
        {}
      ],
      "responseStatus": "string",
      "surveyID": 1,
      "surveyName": "Ava Chen",
      "timestamp": "string",
      "timeTaken": 1,
      "utctimestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browser` | string |  |
| `currentInset` | string |  |
| `customVariables` | object |  |
| `dataQuality` | string |  |
| `dataQualityScore` | number |  |
| `duplicate` | boolean |  |
| `externalReference` | string |  |
| `language` | string |  |
| `location` | object |  |
| `operatingSystem` | string |  |
| `osDeviceType` | string |  |
| `responseID` | number |  |
| `responseSet` | array<object> |  |
| `responseStatus` | string |  |
| `surveyID` | number |  |
| `surveyName` | string |  |
| `timestamp` | string |  |
| `timeTaken` | number |  |
| `utctimestamp` | number |  |

## Native endpoint

Through the native QuestionPro Surveys API, this operation is `GET surveys/:surveyId/responses` (base URL `https://api.questionpro.com/a/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-responses.md) for the provider-specific parameters and requirements.

