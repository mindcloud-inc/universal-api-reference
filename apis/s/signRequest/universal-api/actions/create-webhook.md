# SignRequest: Create Webhook



```
POST https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignRequest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventType": "signed",
  "callbackUrl": "https://example.com/webhooks/signrequest"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventType": "signed",
    "callbackUrl": "https://example.com/webhooks/signrequest"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Example: `Contract events`. |
| `eventType` | list<string> | yes | One of: `cancelled`, `convert_error`, `converted`, `declined`, `downloaded`, `expired`, `login_failed`, `login_successful`, `password_reset_request_error`, `password_reset_request_sent`, `sending_error`, `sent`, `signed`, `signer_downloaded`, `signer_email_bounced`, `signer_forwarded`, `signer_signed`, `signer_viewed`, `signer_viewed_email`, `signrequest_received`, `viewed`. Example: `signed`. |
| `callbackUrl` | string | yes | Example: `https://example.com/webhooks/signrequest`. |
| `integration` | list<string> | no | One of: `formdesk`, `mfiles`, `microsoft-flow`, `salesforce`, `zapier`. Example: `zapier`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callbackUrl": "https://example.com",
      "created": "2026-05-07T12:00:00.000Z",
      "eventType": "string",
      "integration": "string",
      "name": "Ava Chen",
      "url": "https://example.com",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackUrl` | string |  |
| `created` | date |  |
| `eventType` | string |  |
| `integration` | string |  |
| `name` | string |  |
| `url` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native SignRequest API, this operation is `POST /webhooks/` (base URL `https://signrequest.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

