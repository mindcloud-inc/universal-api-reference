# Survalyzer: Get Interview



```
GET https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/get-interview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survalyzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/get-interview?connectionId=$CONNECTION_ID&tenant=string&surveyId=1&interviewId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tenant": "string",
  "surveyId": "1",
  "interviewId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/get-interview?${params}`, {
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
| `tenant` | string | yes | Tenant code for the interview request. |
| `surveyId` | number | yes | Survey identifier that owns the interview. |
| `interviewId` | string | yes | Interview identifier to read. |
| `loadSurveyDefinition` | boolean | no | Whether to include survey definition in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorCode": "string",
      "errorMessage": "string",
      "isSuccess": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorCode` | string |  |
| `errorMessage` | string |  |
| `isSuccess` | boolean |  |

## Native endpoint

Through the native Survalyzer API, this operation is `POST /publicapi/Interview/v3/ReadInterview` (base URL `https://api.survalyzer-eu.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-interview.md) for the provider-specific parameters and requirements.

