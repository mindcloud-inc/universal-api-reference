# Groq: Create Fine Tuning

Creates a fine-tuning job in Groq.

```
POST https://connect.mindcloud.co/v1/universal/groq/latest/actions/create-fine-tuning
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Groq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/groq/latest/actions/create-fine-tuning" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/groq/latest/actions/create-fine-tuning', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputFileId` | string | no |  |
| `name` | string | no |  |
| `type` | string | no |  |
| `baseModel` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseModel": "string",
      "createdAt": 1,
      "fineTunedModel": "string",
      "id": "string",
      "inputFileId": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseModel` | string |  |
| `createdAt` | number |  |
| `fineTunedModel` | string |  |
| `id` | string |  |
| `inputFileId` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Groq API, this operation is `POST /v1/fine_tunings` (base URL `https://api.groq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-fine-tuning.md) for the provider-specific parameters and requirements.

