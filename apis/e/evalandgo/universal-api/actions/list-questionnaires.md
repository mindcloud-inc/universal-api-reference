# Evalandgo: List Questionnaires

Retrieves questionnaires from Evalandgo.

```
GET https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/list-questionnaires
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evalandgo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/list-questionnaires?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/list-questionnaires?${params}`, {
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
| `name` | string | no |  |
| `active` | boolean | no |  |
| `blocked` | boolean | no |  |
| `visible` | boolean | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderCreateAt` | string | no |  |
| `orderId` | string | no |  |

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
          "active": true,
          "createAt": "string",
          "endDateTime": {},
          "id": 1,
          "label": {},
          "name": "Ava Chen",
          "nonStartedRespondentsCount": 1,
          "numberRespondent": 1,
          "questionnaireUrl": {},
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
| `hydra:member[].active` | boolean |  |
| `hydra:member[].createAt` | string |  |
| `hydra:member[].endDateTime` | object |  |
| `hydra:member[].id` | number |  |
| `hydra:member[].label` | object |  |
| `hydra:member[].name` | string |  |
| `hydra:member[].nonStartedRespondentsCount` | number |  |
| `hydra:member[].numberRespondent` | number |  |
| `hydra:member[].questionnaireUrl` | object |  |
| `hydra:member[].questions[].@id` | string |  |
| `hydra:member[].questions[].@type` | string |  |
| `hydra:member[].questions[].id` | number |  |
| `hydra:member[].questions[].label` | string |  |
| `hydra:member[].questions[].position` | number |  |
| `hydra:member[].startDateTime` | object |  |
| `hydra:member[].updatedAt` | string |  |
| `hydra:search.@type` | string |  |
| `hydra:search.hydra:mapping[].@type` | string |  |
| `hydra:search.hydra:mapping[].property` | string |  |
| `hydra:search.hydra:mapping[].required` | boolean |  |
| `hydra:search.hydra:mapping[].variable` | string |  |
| `hydra:search.hydra:template` | string |  |
| `hydra:search.hydra:variableRepresentation` | string |  |
| `hydra:totalItems` | number |  |

## Native endpoint

Through the native Evalandgo API, this operation is `GET /api/v3/questionnaires` (base URL `https://app.evalandgo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-questionnaires.md) for the provider-specific parameters and requirements.

