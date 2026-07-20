# Maildrip: Delete a user's card



```
DELETE https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/delete-a-user-s-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/delete-a-user-s-card?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/delete-a-user-s-card?${params}`, {
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
| `id` | string | yes | The payment method ID of the card to delete |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cards": [
        {}
      ],
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cards` | array<object> |  |
| `message` | string |  |

## Native endpoint

Through the native Maildrip API, this operation is `DELETE /api/v1/payment/stripe/customer/cards/{id}` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-user-s-card.md) for the provider-specific parameters and requirements.

