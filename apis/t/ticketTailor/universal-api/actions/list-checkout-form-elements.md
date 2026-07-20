# Ticket Tailor: List Checkout Form Elements

Retrieves checkout form elements from Ticket Tailor.

```
GET https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-checkout-form-elements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticket Tailor `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-checkout-form-elements?connectionId=$CONNECTION_ID&limit=25&offset=0&checkoutFormId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "checkoutFormId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketTailor/latest/actions/list-checkout-form-elements?${params}`, {
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
| `checkoutFormId` | string | yes | Ticket Tailor checkout form ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checkoutFormId": "string",
      "id": "string",
      "object": "string",
      "options": [
        "string"
      ],
      "perTicket": "string",
      "question": "string",
      "required": "string",
      "termsAndConditions": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkoutFormId` | string | A unique identifier for the checkout form |
| `id` | string | A unique identifier for the checkout form element |
| `object` | string |  |
| `options` | array<string> | List of possible answers for the element |
| `perTicket` | string | Whether the checkout form element is asked globally or per ticket |
| `question` | string | The question to be answered |
| `required` | string | Indicates whether the question is required to answer |
| `termsAndConditions` | string | The HTML content for Terms & Conditions elements (termsCheckbox and termsSignature types only). Returns null for other element types. |
| `type` | string | The type of the checkout form element |

## Native endpoint

Through the native Ticket Tailor API, this operation is `GET /v1/checkout_forms/:checkout_form_id/elements` (base URL `https://api.tickettailor.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-checkout-form-elements.md) for the provider-specific parameters and requirements.

