# Evalandgo: Retrieve Form Question

Retrieves a form question from Evalandgo.

```
GET https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/retrieve-form-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evalandgo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/retrieve-form-question?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/retrieve-form-question?${params}`, {
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
| `id` | string | yes | Question form identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "connected": true,
      "correction": true,
      "explanation": {},
      "explanationFalse": {},
      "help": {},
      "id": 1,
      "inputs": [
        {
          "@id": "string",
          "@type": "string",
          "connected": true,
          "connection": "string",
          "field": {},
          "id": 1,
          "label": "string",
          "type": "string"
        }
      ],
      "label": "string",
      "page": "string",
      "personalData": true,
      "point": 1,
      "position": 1,
      "questionName": "Ava Chen",
      "quiz": true,
      "required": true
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
| `connected` | boolean |  |
| `correction` | boolean |  |
| `explanation` | object |  |
| `explanationFalse` | object |  |
| `help` | object |  |
| `id` | number |  |
| `inputs[].@id` | string |  |
| `inputs[].@type` | string |  |
| `inputs[].connected` | boolean |  |
| `inputs[].connection` | string |  |
| `inputs[].field` | object |  |
| `inputs[].id` | number |  |
| `inputs[].label` | string |  |
| `inputs[].type` | string |  |
| `label` | string |  |
| `page` | string |  |
| `personalData` | boolean |  |
| `point` | number |  |
| `position` | number |  |
| `questionName` | string |  |
| `quiz` | boolean |  |
| `required` | boolean |  |

## Native endpoint

Through the native Evalandgo API, this operation is `GET /api/v3/questions/form/:id` (base URL `https://app.evalandgo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-form-question.md) for the provider-specific parameters and requirements.

