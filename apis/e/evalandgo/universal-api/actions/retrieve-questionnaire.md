# Evalandgo: Retrieve Questionnaire

Retrieves a questionnaire from Evalandgo.

```
GET https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/retrieve-questionnaire
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evalandgo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/retrieve-questionnaire?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/retrieve-questionnaire?${params}`, {
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
| `id` | string | yes | Questionnaire identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "active": true,
      "createAt": "string",
      "endDateTime": {},
      "id": 1,
      "label": {},
      "name": "Ava Chen",
      "nonStartedRespondentsCount": 1,
      "numberRespondent": 1,
      "questionnaireUrl": "https://example.com",
      "questions": [
        {
          "@id": "string",
          "@type": "string",
          "id": 1,
          "label": "string",
          "position": 1
        }
      ],
      "startDateTime": {},
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | string |  |
| `@id` | string |  |
| `@type` | string |  |
| `active` | boolean |  |
| `createAt` | string |  |
| `endDateTime` | object |  |
| `id` | number |  |
| `label` | object |  |
| `name` | string |  |
| `nonStartedRespondentsCount` | number |  |
| `numberRespondent` | number |  |
| `questionnaireUrl` | string |  |
| `questions[].@id` | string |  |
| `questions[].@type` | string |  |
| `questions[].id` | number |  |
| `questions[].label` | string |  |
| `questions[].position` | number |  |
| `startDateTime` | object |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Evalandgo API, this operation is `GET /api/v3/questionnaires/:id` (base URL `https://app.evalandgo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-questionnaire.md) for the provider-specific parameters and requirements.

