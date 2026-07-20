# Evalandgo: Update Text Response

Updates an existing text response in Evalandgo.

```
PUT https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/update-text-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evalandgo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/update-text-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/update-text-response', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `text` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "id": 1,
      "personalData": {},
      "position": 1,
      "question": "string",
      "respondent": "string",
      "score": {},
      "text": "string",
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
| `id` | number |  |
| `personalData` | object |  |
| `position` | number |  |
| `question` | string |  |
| `respondent` | string |  |
| `score` | object |  |
| `text` | string |  |
| `timer` | number |  |
| `userEdited` | boolean |  |

## Native endpoint

Through the native Evalandgo API, this operation is `PUT /api/v3/responses/text/:id` (base URL `https://app.evalandgo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-text-response.md) for the provider-specific parameters and requirements.

