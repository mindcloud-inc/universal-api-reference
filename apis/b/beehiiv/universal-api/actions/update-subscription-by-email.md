# Beehiiv: Update Subscription by Email

Updates a subscription in Beehiiv by email address.

```
PUT https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/update-subscription-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beehiiv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/update-subscription-by-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "publicationId": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/update-subscription-by-email', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "publicationId": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `publicationId` | string | yes | The prefixed ID of the publication object. |
| `email` | string | yes | Email address (URL-encoded in path). |
| `newEmail` | string | no | Optional new email address for the subscription. |
| `unsubscribe` | boolean | no | Set true to unsubscribe the subscription. |
| `tier` | string | no | Optional tier update value. |
| `stripeCustomerId` | string | no | Optional Stripe customer identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beehiiv API returns.

## Native endpoint

Through the native Beehiiv API, this operation is `PUT /v2/publications/:publicationId/subscriptions/by_email/:email` (base URL `https://api.beehiiv.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscription-by-email.md) for the provider-specific parameters and requirements.

