# Systeme.io: List Payment Subscriptions

Retrieves payment subscriptions from Systeme.io for a contact.

```
GET https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/list-payment-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Systeme.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/list-payment-subscriptions?connectionId=$CONNECTION_ID&contact=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/list-payment-subscriptions?${params}`, {
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
| `contact` | number | yes | Contact identifier used to fetch subscriptions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMore` | boolean | Whether more pages are available. |
| `items` | array<object> | Subscription records. |

## Native endpoint

Through the native Systeme.io API, this operation is `GET /api/payment/subscriptions` (base URL `https://api.systeme.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payment-subscriptions.md) for the provider-specific parameters and requirements.

