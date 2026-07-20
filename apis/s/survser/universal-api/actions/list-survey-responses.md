# Survser: List Survey Responses



```
GET https://connect.mindcloud.co/v1/universal/survser/latest/actions/list-survey-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/survser/latest/actions/list-survey-responses?connectionId=$CONNECTION_ID&surveyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/survser/latest/actions/list-survey-responses?${params}`, {
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
| `surveyId` | string | yes | The Survser survey ID. Survser docs say you can find it in the survey insights URL `survser.com/surveys/<id>/insights`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "anonIdentifier": "string",
      "complete": true,
      "createdAt": "string",
      "id": "string",
      "responses": [
        {}
      ],
      "survey": "string",
      "updatedAt": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `anonIdentifier` | string | Anonymous respondent identifier when present. |
| `complete` | boolean | Whether the survey response was completed. |
| `createdAt` | string | When the response was created. |
| `id` | string | The response ID. |
| `responses` | array<object> | The per-question answers included in the response. |
| `survey` | string | The related survey ID. |
| `updatedAt` | string | When the response was last updated. |
| `user` | object | Tracked user metadata when present. |

## Native endpoint

Through the native Survser API, this operation is `GET /response/list` (base URL `https://survser.com/api/public/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-survey-responses.md) for the provider-specific parameters and requirements.

