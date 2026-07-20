# Evalandgo: Create Unique Response

Creates a unique response in Evalandgo.

```
POST https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/create-unique-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evalandgo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/create-unique-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "respondent": "string",
  "question": "string",
  "choice": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/create-unique-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "respondent": "string",
    "question": "string",
    "choice": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `respondent` | string | yes |  |
| `question` | string | yes |  |
| `choice` | string | yes |  |
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
      "choice": {
        "@id": "string",
        "@type": "string",
        "correct": true,
        "id": 1,
        "label": "string",
        "labelReport": {},
        "position": 1
      },
      "correct": true,
      "id": 1,
      "personalData": {},
      "position": 1,
      "question": "string",
      "respondent": "string",
      "score": {},
      "text": {},
      "timer": 1,
      "userEdited": true
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
| `choice.@id` | string |  |
| `choice.@type` | string |  |
| `choice.correct` | boolean |  |
| `choice.id` | number |  |
| `choice.label` | string |  |
| `choice.labelReport` | object |  |
| `choice.position` | number |  |
| `correct` | boolean |  |
| `id` | number |  |
| `personalData` | object |  |
| `position` | number |  |
| `question` | string |  |
| `respondent` | string |  |
| `score` | object |  |
| `text` | object |  |
| `timer` | number |  |
| `userEdited` | boolean |  |

## Native endpoint

Through the native Evalandgo API, this operation is `POST /api/v3/responses/unique` (base URL `https://app.evalandgo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-unique-response.md) for the provider-specific parameters and requirements.

