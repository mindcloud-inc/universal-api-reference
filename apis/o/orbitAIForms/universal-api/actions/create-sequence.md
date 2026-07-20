# Orbit AI (Forms): Create Sequence



```
POST https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/create-sequence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orbit AI (Forms) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/create-sequence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/create-sequence', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "status": "string",
      "steps": [
        {}
      ],
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `id` | string |  |
| `status` | string |  |
| `steps` | array<object> |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Orbit AI (Forms) API, this operation is `POST /api/v1/sequences` (base URL `https://orbitforms.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sequence.md) for the provider-specific parameters and requirements.

