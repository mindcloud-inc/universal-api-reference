# Drag'n Survey: Get Respondent Responses

Retrieves responses for a Drag'n Survey respondent.

```
GET https://connect.mindcloud.co/v1/universal/dragnSurvey/latest/actions/get-respondent-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Drag'n Survey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dragnSurvey/latest/actions/get-respondent-responses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dragnSurvey/latest/actions/get-respondent-responses?${params}`, {
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
| `respondentId` | string | no | The Drag'n Survey respondent ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Drag'n Survey API returns.

## Native endpoint

Through the native Drag'n Survey API, this operation is `GET respondents/:respondentId` (base URL `https://developer.dragnsurvey.com/api/v2.0.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-respondent-responses.md) for the provider-specific parameters and requirements.

