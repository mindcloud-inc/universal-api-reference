# Checkout Page: Validate Ticket

Validates a ticket in Checkout Page by QR code.

```
GET https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/validate-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkout Page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/validate-ticket?connectionId=$CONNECTION_ID&qrCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "qrCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/validate-ticket?${params}`, {
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
| `qrCode` | string | yes | Validate ticket |
| `metadata[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true,
      "ticket": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `success` | boolean |  |
| `ticket` | object |  |

## Native endpoint

Through the native Checkout Page API, this operation is `POST /v1/tickets/validate/:qrCode` (base URL `https://api.checkoutpage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-ticket.md) for the provider-specific parameters and requirements.

