# Evalandgo: List Questionnaire Questions

Retrieves questions for a questionnaire from Evalandgo.

```
GET https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/list-questionnaire-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evalandgo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/list-questionnaire-questions?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/list-questionnaire-questions?${params}`, {
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
      "hydra:member": [
        {
          "@id": "string",
          "@type": "string",
          "correction": true,
          "explanation": {},
          "explanationFalse": {},
          "help": {},
          "id": 1,
          "label": "string",
          "maximumCharacters": {},
          "minimumCharacters": {},
          "page": "string",
          "personalData": true,
          "point": 1,
          "position": 1,
          "questionName": "Ava Chen",
          "quiz": true,
          "required": true
        }
      ],
      "hydra:search": {
        "@type": "string",
        "hydra:mapping": [
          {
            "@type": "string",
            "property": "string",
            "required": true,
            "variable": "string"
          }
        ],
        "hydra:template": "string",
        "hydra:variableRepresentation": "string"
      },
      "hydra:totalItems": 1
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
| `hydra:member[].@id` | string |  |
| `hydra:member[].@type` | string |  |
| `hydra:member[].correction` | boolean |  |
| `hydra:member[].explanation` | object |  |
| `hydra:member[].explanationFalse` | object |  |
| `hydra:member[].help` | object |  |
| `hydra:member[].id` | number |  |
| `hydra:member[].label` | string |  |
| `hydra:member[].maximumCharacters` | object |  |
| `hydra:member[].minimumCharacters` | object |  |
| `hydra:member[].page` | string |  |
| `hydra:member[].personalData` | boolean |  |
| `hydra:member[].point` | number |  |
| `hydra:member[].position` | number |  |
| `hydra:member[].questionName` | string |  |
| `hydra:member[].quiz` | boolean |  |
| `hydra:member[].required` | boolean |  |
| `hydra:search.@type` | string |  |
| `hydra:search.hydra:mapping[].@type` | string |  |
| `hydra:search.hydra:mapping[].property` | string |  |
| `hydra:search.hydra:mapping[].required` | boolean |  |
| `hydra:search.hydra:mapping[].variable` | string |  |
| `hydra:search.hydra:template` | string |  |
| `hydra:search.hydra:variableRepresentation` | string |  |
| `hydra:totalItems` | number |  |

## Native endpoint

Through the native Evalandgo API, this operation is `GET /api/v3/questionnaires/:id/questions` (base URL `https://app.evalandgo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-questionnaire-questions.md) for the provider-specific parameters and requirements.

