# Stripe: Retrieve Event



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-event?connectionId=$CONNECTION_ID&event=evt_..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "event": "evt_..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-event?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event` | string | yes | Example: `evt_...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiVersion": "string",
      "created": 1,
      "data": {},
      "id": "string",
      "livemode": true,
      "pendingWebhooks": 1,
      "request": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | string |  |
| `created` | number |  |
| `data` | object |  |
| `id` | string |  |
| `livemode` | boolean |  |
| `pendingWebhooks` | number |  |
| `request` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Stripe API, this operation is `GET events/:event` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-event.md) for the provider-specific parameters and requirements.

