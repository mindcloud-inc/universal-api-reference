# Fidel API: Create Webhook (Program)

Creates a webhook for a Fidel program.

```
POST https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/create-webhook-program
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/create-webhook-program" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "programId": "string",
  "event": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/create-webhook-program', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `programId` | string | yes |  |
| `event` | string | yes | The webhook event type. |
| `url` | string | yes | URL destination of the event. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `offerId` | string | no | Optional offer ID filter for qualified auth and clearing transaction events. |

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
      "url": "https://example.com"
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

## Native endpoint

Through the native Fidel API API, this operation is `POST /programs/:programId/hooks` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-program.md) for the provider-specific parameters and requirements.

