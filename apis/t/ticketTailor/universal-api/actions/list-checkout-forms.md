# Ticket Tailor: List Checkout Forms

Retrieves checkout forms from Ticket Tailor.

```
GET https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-checkout-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticket Tailor `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-checkout-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-checkout-forms?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "checkoutFormElements": [
        "string"
      ],
      "createdAt": 1,
      "eventSeriesId": "string",
      "id": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkoutFormElements` | array<string> | List of custom form elements ids |
| `createdAt` | number | Timestamp when the checkout form was created |
| `eventSeriesId` | string | A unique identifier for the event series this checkout form is associated with |
| `id` | string | A unique identifier for the checkout form |
| `object` | string |  |

## Native endpoint

Through the native Ticket Tailor API, this operation is `GET /v1/checkout_forms` (base URL `https://api.tickettailor.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-checkout-forms.md) for the provider-specific parameters and requirements.

