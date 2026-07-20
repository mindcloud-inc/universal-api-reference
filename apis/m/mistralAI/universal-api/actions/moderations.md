# Mistral AI: Moderations

Creates text moderation results in Mistral AI.

```
POST https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/moderations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mistral AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/moderations" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "input[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/moderations', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "input[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | ID of the model to use. |
| `input[]` | array<string> | yes | Text inputs to moderate. |
| `metadata` | object | no | Optional metadata object for the request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "model": "string",
      "results": [
        {}
      ],
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `model` | string |  |
| `results` | array<object> |  |
| `usage` | object |  |

## Native endpoint

Through the native Mistral AI API, this operation is `POST /v1/moderations` (base URL `https://api.mistral.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/moderations.md) for the provider-specific parameters and requirements.

