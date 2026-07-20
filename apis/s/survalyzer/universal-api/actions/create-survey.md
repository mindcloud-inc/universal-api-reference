# Survalyzer: Create Survey



```
POST https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/create-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survalyzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/create-survey" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "name": "Ava Chen",
  "surveyDefinition": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/create-survey', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "name": "Ava Chen",
    "surveyDefinition": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | number | yes |  |
| `name` | string | yes |  |
| `surveyDefinition` | object | yes |  |
| `surveyConfiguration` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorCode": "string",
      "errorMessage": "string",
      "isSuccess": true,
      "surveyId": 1
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
| `surveyId` | number | Identifier of the created survey. |

## Native endpoint

Through the native Survalyzer API, this operation is `POST /publicapi/Survey/v3/CreateSurvey` (base URL `https://api.survalyzer-eu.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-survey.md) for the provider-specific parameters and requirements.

