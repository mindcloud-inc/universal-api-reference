# EventSquare: Register Make Webhook

Registers a Make webhook in EventSquare.

```
POST https://connect.mindcloud.co/v1/universal/eventSquare/latest/actions/register-make-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EventSquare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventSquare/latest/actions/register-make-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "0",
  "url": "https://example.com/webhooks/eventsquare"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventSquare/latest/actions/register-make-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "0",
    "url": "https://example.com/webhooks/eventsquare"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | The EventSquare trigger type to register a webhook for. One of: `0`. |
| `url` | string | yes | The public URL EventSquare should call when the selected trigger fires. Example: `https://example.com/webhooks/eventsquare`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Success status returned after the webhook is registered. |

## Native endpoint

Through the native EventSquare API, this operation is `POST /1.0/integrations/make/triggers` (base URL `https://api.eventsquare.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/register-make-webhook.md) for the provider-specific parameters and requirements.

