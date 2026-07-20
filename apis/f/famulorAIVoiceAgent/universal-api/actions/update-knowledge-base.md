# Famulor AI - Voice Agent: Update Knowledge Base

Updates an existing knowledge base in Famulor.

```
PUT https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/update-knowledge-base
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Famulor AI - Voice Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/update-knowledge-base" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/update-knowledge-base', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Knowledge base description. |
| `id` | number | yes | Famulor knowledge base ID. |
| `name` | string | no | Knowledge base name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Updated knowledge base details. |
| `message` | string | Result message. |

## Native endpoint

Through the native Famulor AI - Voice Agent API, this operation is `PUT /user/knowledgebases/:id` (base URL `https://app.famulor.de/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-knowledge-base.md) for the provider-specific parameters and requirements.

