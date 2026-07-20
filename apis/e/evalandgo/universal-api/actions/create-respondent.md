# Evalandgo: Create Respondent

Creates a new respondent in Evalandgo.

```
POST https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/create-respondent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evalandgo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/create-respondent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "questionnaire": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/create-respondent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "questionnaire": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `questionnaire` | string | yes | Questionnaire IRI, for example /api/v3/questionnaires/123 |
| `email` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | no |  |
| `startAt` | string | no |  |
| `language` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "blocked": true,
      "contact": {},
      "email": "ava@example.com",
      "endAt": {},
      "finish": true,
      "firstName": {},
      "id": 1,
      "identifier": "string",
      "language": {},
      "lastName": {},
      "perfectScore": {},
      "preview": true,
      "questionnaire": "string",
      "questionnaireUrl": "https://example.com",
      "resultUrl": "https://example.com",
      "score": {},
      "source": {},
      "startAt": {},
      "timerGlobal": {}
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
| `blocked` | boolean |  |
| `contact` | object |  |
| `email` | string |  |
| `endAt` | object |  |
| `finish` | boolean |  |
| `firstName` | object |  |
| `id` | number |  |
| `identifier` | string |  |
| `language` | object |  |
| `lastName` | object |  |
| `perfectScore` | object |  |
| `preview` | boolean |  |
| `questionnaire` | string |  |
| `questionnaireUrl` | string |  |
| `resultUrl` | string |  |
| `score` | object |  |
| `source` | object |  |
| `startAt` | object |  |
| `timerGlobal` | object |  |

## Native endpoint

Through the native Evalandgo API, this operation is `POST /api/v3/respondents` (base URL `https://app.evalandgo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-respondent.md) for the provider-specific parameters and requirements.

