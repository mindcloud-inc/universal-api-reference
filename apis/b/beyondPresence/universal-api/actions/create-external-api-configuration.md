# Beyond Presence: Create External API Configuration

Creates a new external API configuration in Beyond Presence.

```
POST https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/create-external-api-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beyond Presence `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/create-external-api-configuration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "apiKey": "string",
  "name": "Ava Chen",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/create-external-api-configuration', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "apiKey": "string",
    "name": "Ava Chen",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apiKey` | string | yes | API key for the external API. |
| `name` | string | yes | Name of the external API configuration. |
| `type` | string | no | External API type. Default: `openai_compatible_llm`. |
| `url` | string | yes | URL of the external API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Unique identifier of the external API configuration. |
| `name` | string | Name of the external API configuration. |
| `type` | string | External API type. |
| `url` | string | External API URL. |

## Native endpoint

Through the native Beyond Presence API, this operation is `POST /v1/external-apis` (base URL `https://api.bey.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-external-api-configuration.md) for the provider-specific parameters and requirements.

