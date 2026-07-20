# Wikibot: Set Webhook URL

Updates the webhook URL in Wikibot.

```
PUT https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/set-webhook-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wikibot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/set-webhook-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/webhooks/wikibot"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/set-webhook-url', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/webhooks/wikibot"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Webhook URL to call for asynchronous results. Example: `https://example.com/webhooks/wikibot`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether Wikibot accepted the webhook URL update. |

## Native endpoint

Through the native Wikibot API, this operation is `POST /bot/set-webhook-url` (base URL `https://api.wikibot.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-webhook-url.md) for the provider-specific parameters and requirements.

