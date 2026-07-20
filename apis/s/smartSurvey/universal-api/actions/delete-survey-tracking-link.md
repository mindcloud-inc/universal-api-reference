# SmartSurvey: Delete Survey Tracking Link

Deletes an existing survey tracking link from SmartSurvey.

```
DELETE https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/delete-survey-tracking-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSurvey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/delete-survey-tracking-link?connectionId=$CONNECTION_ID&surveyId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/delete-survey-tracking-link?${params}`, {
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
| `surveyId` | number | yes | The survey id whose links you are querying |
| `id` | number | yes | The tracking link id that you want to delete |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native SmartSurvey API, this operation is `DELETE /surveys/{surveyId}/links/{id}` (base URL `https://api.smartsurvey.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-survey-tracking-link.md) for the provider-specific parameters and requirements.

