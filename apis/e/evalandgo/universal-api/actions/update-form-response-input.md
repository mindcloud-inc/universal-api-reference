# Evalandgo: Update Form Response Input

Updates an input in a form response in Evalandgo.

```
PUT https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/update-form-response-input
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evalandgo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/update-form-response-input" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "responseId": "string",
  "inputId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/update-form-response-input', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "responseId": "string",
    "inputId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `responseId` | string | yes |  |
| `inputId` | string | yes |  |
| `text` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "input": "string",
      "response": {
        "@id": "string",
        "@type": "string",
        "id": 1,
        "personalData": {},
        "position": 1,
        "question": "string",
        "respondent": "string",
        "responseInputs": [
          "string"
        ],
        "score": {},
        "timer": 1,
        "userEdited": true
      },
      "text": "string"
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
| `input` | string |  |
| `response.@id` | string |  |
| `response.@type` | string |  |
| `response.id` | number |  |
| `response.personalData` | object |  |
| `response.position` | number |  |
| `response.question` | string |  |
| `response.respondent` | string |  |
| `response.responseInputs[]` | string |  |
| `response.score` | object |  |
| `response.timer` | number |  |
| `response.userEdited` | boolean |  |
| `text` | string |  |

## Native endpoint

Through the native Evalandgo API, this operation is `PUT /api/v3/responses/form/:responseId/inputs/:inputId` (base URL `https://app.evalandgo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-response-input.md) for the provider-specific parameters and requirements.

