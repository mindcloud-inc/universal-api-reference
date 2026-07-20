# Groq: Create Translation

Creates an audio translation in Groq.

```
POST https://connect.mindcloud.co/v1/universal/groq/latest/actions/create-translation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Groq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/groq/latest/actions/create-translation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/groq/latest/actions/create-translation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | no |  |
| `url` | string | no |  |
| `model` | string | yes |  |
| `responseFormat` | list | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | no |  |
| `temperature` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "text": "string",
      "xGroq": {
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `text` | string |  |
| `xGroq.id` | string |  |

## Native endpoint

Through the native Groq API, this operation is `POST /openai/v1/audio/translations` (base URL `https://api.groq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-translation.md) for the provider-specific parameters and requirements.

