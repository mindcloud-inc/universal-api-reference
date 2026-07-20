# Insighto.ai: Add Intent To Assistant



```
PUT https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/add-intent-to-assistant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insighto.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/add-intent-to-assistant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assistantId": "3c90c3cc-0d44-4b50-8888-8dd25736052a",
  "intentId": "3c90c3cc-0d44-4b50-8888-8dd25736052a"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/add-intent-to-assistant', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assistantId": "3c90c3cc-0d44-4b50-8888-8dd25736052a",
    "intentId": "3c90c3cc-0d44-4b50-8888-8dd25736052a"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assistantId` | string | yes | The UUID id of the assistant. Example: `3c90c3cc-0d44-4b50-8888-8dd25736052a`. |
| `intentId` | string | yes | The UUID id of the intent. Example: `3c90c3cc-0d44-4b50-8888-8dd25736052a`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assistant_id": "string",
      "attributes": {},
      "id": "string",
      "intent_id": "string",
      "is_active": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assistant_id` | string |  |
| `attributes` | object |  |
| `id` | string |  |
| `intent_id` | string |  |
| `is_active` | boolean |  |

## Native endpoint

Through the native Insighto.ai API, this operation is `POST /assistant/:assistant_id/intent/:intent_id` (base URL `https://api.insighto.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-intent-to-assistant.md) for the provider-specific parameters and requirements.

