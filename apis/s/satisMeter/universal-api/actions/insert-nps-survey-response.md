# SatisMeter: Insert NPS Survey Response



```
POST https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/insert-nps-survey-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SatisMeter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/insert-nps-survey-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "writeKey": "string",
  "userId": "string",
  "score": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/insert-nps-survey-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "writeKey": "string",
    "userId": "string",
    "score": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `writeKey` | string | yes | SatisMeter survey write key for response insertion. |
| `userId` | string | yes | External user identifier for the disposable or real survey respondent. |
| `score` | number | yes | NPS score value for the rating question. |
| `comment` | string | no | Free-text answer for the comment question. |
| `name` | string | no | Optional respondent name sent into traits. |
| `email` | string | no | Optional respondent email sent into traits. |
| `forceSurvey` | boolean | no | When true, allows creating the response even if survey rules would normally suppress it. Default: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SatisMeter API returns.

## Native endpoint

Through the native SatisMeter API, this operation is `POST /api/responses` (base URL `https://app.satismeter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-nps-survey-response.md) for the provider-specific parameters and requirements.

