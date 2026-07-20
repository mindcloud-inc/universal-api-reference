# Colossyan: Generate Draft From Knowledge

Creates a draft from structured knowledge in Colossyan.

```
POST https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/generate-draft-from-knowledge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Colossyan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/generate-draft-from-knowledge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "summary": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/generate-draft-from-knowledge', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "summary": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `summary` | object | yes | Structured summary object with title, description, and chapters. |
| `templateId` | string | no | Optional template ID for the generated draft. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string | Colossyan draft URL generated from the supplied knowledge summary. |

## Native endpoint

Through the native Colossyan API, this operation is `POST https://app.colossyan.com/api/knowledge-to-draft/generate-draft` (base URL `https://app.colossyan.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-draft-from-knowledge.md) for the provider-specific parameters and requirements.

