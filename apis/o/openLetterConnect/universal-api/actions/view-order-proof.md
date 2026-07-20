# Open Letter Connect: View Order Proof

Retrieves an order proof from Open Letter Connect.

```
GET https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/view-order-proof
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Letter Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/view-order-proof?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/view-order-proof?${params}`, {
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
| `orderId` | string | no | The existing order ID to generate a proof for. |
| `templateId` | number | no | The template ID to render a proof for. |
| `contactId` | number | no | The contact ID to render in the proof. |
| `returnContactId` | number | no | The return contact ID to use for the proof. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "base64": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.base64` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Open Letter Connect API, this operation is `POST /orders/view-proof` (base URL `https://api.openletterconnect.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-order-proof.md) for the provider-specific parameters and requirements.

