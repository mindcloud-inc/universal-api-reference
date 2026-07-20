# Stripe: List Payouts



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/new-action1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/new-action1?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/new-action1?${params}`, {
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
| `stripeApiKey` | string | no |  |
| `arrivalDateGte` | string | no |  |
| `arrivalDateLte` | string | no |  |
| `status` | string | no |  |
| `limit` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Stripe API returns.

## Native endpoint

Through the native Stripe API, this operation is `GET /payouts?arrival_date[gte]={{arrivalDateGte}}&arrival_date[lte]={{arrivalDateLte}}&status={{status}}&limit={{limit}}` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/new-action1.md) for the provider-specific parameters and requirements.

