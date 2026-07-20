# Fidel API: Update Webhook

Updates an existing webhook in Fidel API.

```
PUT https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hookId": "string",
  "programId": "string",
  "event": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hookId": "string",
    "programId": "string",
    "event": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hookId` | string | yes |  |
| `programId` | string | yes | The program ID. |
| `event` | string | yes | The webhook event. |
| `url` | string | yes | The destination URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "event": "string",
      "id": "string",
      "live": true,
      "programId": "string",
      "secretKey": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `created` | date |  |
| `event` | string |  |
| `id` | string |  |
| `live` | boolean |  |
| `programId` | string |  |
| `secretKey` | string |  |
| `updated` | date |  |
| `url` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Fidel API API, this operation is `PATCH /hooks/:hookId` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

