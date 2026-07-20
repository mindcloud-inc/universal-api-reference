# Fathom: Create Webhook

Creates a new webhook in Fathom.

```
POST https://connect.mindcloud.co/v1/universal/fathom/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fathom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fathom/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destinationUrl": "https://example.com",
  "triggeredFor[]": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fathom/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destinationUrl": "https://example.com",
    "triggeredFor[]": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `destinationUrl` | string | yes | Webhook destination URL. |
| `triggeredFor[]` | array<string> | yes | One or more webhook scopes. Allowed: my_recordings, shared_with_me, internal_meetings, external_meetings, all_recordings. One of: `0`, `1`, `2`, `3`, `4`. |
| `includeActionItems` | boolean | no | Include action items in webhook payload. |
| `includeCrmMatches` | boolean | no | Include CRM matches in webhook payload. |
| `includeSummary` | boolean | no | Include summary in webhook payload. |
| `includeTranscript` | boolean | no | Include transcript in webhook payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "includeActionItems": true,
      "includeCrmMatches": true,
      "includeSummary": true,
      "includeTranscript": true,
      "secret": "string",
      "triggeredFor": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `includeActionItems` | boolean |  |
| `includeCrmMatches` | boolean |  |
| `includeSummary` | boolean |  |
| `includeTranscript` | boolean |  |
| `secret` | string |  |
| `triggeredFor` | array<string> |  |
| `url` | string |  |

## Native endpoint

Through the native Fathom API, this operation is `POST /webhooks` (base URL `https://api.fathom.ai/external/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

