# QuestionPro Surveys: Get Response Filter



```
GET https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-response-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuestionPro Surveys `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-response-filter?connectionId=$CONNECTION_ID&surveyId=13483869" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "13483869"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-response-filter?${params}`, {
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
| `surveyId` | number | yes | QuestionPro survey ID. Example: `13483869`. |
| `page` | number | no | Page number. Example: `1`. |
| `perPage` | number | no | Results per page. Example: `100`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `extRef` | string | no | Filter responses by external reference. Example: `Marketing`. |
| `custom1` | string | no | Filter responses by custom1. Example: `Content`. |
| `custom2` | string | no | Filter responses by custom2. |
| `custom3` | string | no | Filter responses by custom3. |
| `custom4` | string | no | Filter responses by custom4. |
| `custom5` | string | no | Filter responses by custom5. |

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

Through the native QuestionPro Surveys API, this operation is `GET surveys/:surveyId/responses/filter` (base URL `https://api.questionpro.com/a/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-response-filter.md) for the provider-specific parameters and requirements.

