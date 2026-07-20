# Stripe: List Checkout Session Line Items

Retrieves line items for a Stripe checkout session.

```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-checkout-session-line-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-checkout-session-line-items?connectionId=$CONNECTION_ID&limit=25&offset=0&session=cs_test_a1b2c3d4" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "session": "cs_test_a1b2c3d4"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/list-checkout-session-line-items?${params}`, {
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
| `session` | string | yes | Checkout Session identifier. Example: `cs_test_a1b2c3d4`. |
| `limit` | number | no | Number of line items to return (1-100). Example: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startingAfter` | string | no | Cursor for forward pagination. |
| `endingBefore` | string | no | Cursor for reverse pagination. |
| `expand` | list<string> | no | Fields to expand in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "hasMore": true,
      "object": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `hasMore` | boolean |  |
| `object` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Stripe API, this operation is `GET checkout/sessions/:session/line_items` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-checkout-session-line-items.md) for the provider-specific parameters and requirements.

