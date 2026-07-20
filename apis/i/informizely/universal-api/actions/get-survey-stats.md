# Informizely: Get Survey Stats



```
GET https://connect.mindcloud.co/v1/universal/informizely/latest/actions/get-survey-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Informizely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/informizely/latest/actions/get-survey-stats?connectionId=$CONNECTION_ID&surveyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/informizely/latest/actions/get-survey-stats?${params}`, {
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
| `surveyId` | string | yes | The ID of the survey whose statistics you want to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "FirstEventTime": "2026-05-07T12:00:00.000Z",
      "LastEventTime": "2026-05-07T12:00:00.000Z",
      "NrCompleted": 1,
      "NrDeleted": 1,
      "NrEmptyClosedExplicit": 1,
      "NrEmptyClosedImplicit": 1,
      "NrEmptyCompleted": 1,
      "NrOpened": 1,
      "NrResponses": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `FirstEventTime` | date | The timestamp of the first recorded survey event. |
| `LastEventTime` | date | The timestamp of the last recorded survey event. |
| `NrCompleted` | number | The number of completed non-empty responses. |
| `NrDeleted` | number | The number of deleted responses. |
| `NrEmptyClosedExplicit` | number | The number of explicit closes without answers. |
| `NrEmptyClosedImplicit` | number | The number of implicit closes without answers. |
| `NrEmptyCompleted` | number | The number of empty completed responses. |
| `NrOpened` | number | The number of times the survey was displayed. |
| `NrResponses` | number | The total number of non-empty responses. |

## Native endpoint

Through the native Informizely API, this operation is `GET /stats` (base URL `https://api.informizely.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey-stats.md) for the provider-specific parameters and requirements.

