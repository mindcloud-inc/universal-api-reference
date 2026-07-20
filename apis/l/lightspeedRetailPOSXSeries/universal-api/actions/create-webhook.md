# Lightspeed Retail POS (X-Series): Create Webhook

Creates a new webhook in Lightspeed Retail POS (X-Series).

```
POST https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightspeed Retail POS (X-Series) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "type": "string",
  "active": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "type": "string",
    "active": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The destination URL for webhook deliveries. |
| `type` | string | yes | The webhook event type. |
| `active` | boolean | yes | Whether the webhook is active. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": "string",
      "id": "string",
      "retailerId": "string",
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
| `active` | string |  |
| `id` | string |  |
| `retailerId` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Lightspeed Retail POS (X-Series) API, this operation is `POST /api/2.0/webhooks` (base URL `https://{{credentials.authorizeRequest.domain_prefix}}.retail.lightspeed.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

