# Dwolla: Get Webhook Subscription

Retrieves a webhook subscription from Dwolla.

```
GET https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dwolla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-webhook-subscription?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-webhook-subscription?${params}`, {
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
| `id` | string | no | Dwolla webhook subscription ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "created": "string",
      "id": "string",
      "paused": true,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | HAL links for related webhook resources. |
| `created` | string | Webhook-subscription creation timestamp. |
| `id` | string | Dwolla webhook-subscription identifier. |
| `paused` | boolean | Whether delivery is paused. |
| `url` | string | Webhook delivery URL. |

## Native endpoint

Through the native Dwolla API, this operation is `GET /webhook-subscriptions/[:id]` (base URL `https://api-sandbox.dwolla.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-subscription.md) for the provider-specific parameters and requirements.

