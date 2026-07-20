# Drag'n Survey: List Survey Collectors

Retrieves collectors for a Drag'n Survey survey.

```
GET https://connect.mindcloud.co/v1/universal/dragnSurvey/latest/actions/list-survey-collectors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Drag'n Survey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dragnSurvey/latest/actions/list-survey-collectors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dragnSurvey/latest/actions/list-survey-collectors?${params}`, {
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
| `surveyId` | string | no | The Drag'n Survey survey ID. |
| `title_contains` | string | no | Filter collectors whose title contains this text. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Drag'n Survey API returns.

## Native endpoint

Through the native Drag'n Survey API, this operation is `GET surveys/:surveyId/collectors` (base URL `https://developer.dragnsurvey.com/api/v2.0.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-survey-collectors.md) for the provider-specific parameters and requirements.

