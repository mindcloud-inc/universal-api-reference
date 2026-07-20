# Cloudprinter.com: Add Order

Creates an order in Cloudprinter.com.

```
POST https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/add-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudprinter.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/add-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reference": "string",
  "email": "ava@example.com",
  "addresses[]": [
    {}
  ],
  "addresses[].type": "delivery",
  "addresses[].firstname": "Ava",
  "addresses[].lastname": "Chen",
  "addresses[].street1": "string",
  "addresses[].zip": "string",
  "addresses[].city": "string",
  "addresses[].country": "string",
  "addresses[].email": "ava@example.com",
  "addresses[].phone": "string",
  "items[]": [
    {}
  ],
  "items[].reference": "string",
  "items[].product": "string",
  "items[].count": "string",
  "items[].files[]": [
    {}
  ],
  "items[].files[].type": "string",
  "items[].files[].url": "https://example.com",
  "items[].files[].md5sum": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/add-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reference": "string",
    "email": "ava@example.com",
    "addresses[]": [{}],
    "addresses[].type": "delivery",
    "addresses[].firstname": "Ava",
    "addresses[].lastname": "Chen",
    "addresses[].street1": "string",
    "addresses[].zip": "string",
    "addresses[].city": "string",
    "addresses[].country": "string",
    "addresses[].email": "ava@example.com",
    "addresses[].phone": "string",
    "items[]": [{}],
    "items[].reference": "string",
    "items[].product": "string",
    "items[].count": "string",
    "items[].files[]": [{}],
    "items[].files[].type": "string",
    "items[].files[].url": "https://example.com",
    "items[].files[].md5sum": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reference` | string | yes | Client order reference. |
| `email` | string | yes | Customer email address for the order. |
| `addresses[]` | array<object> | yes | One or more delivery addresses. |
| `addresses[].type` | string | yes | Address type. Cloudprinter expects delivery for order creation. Default: `delivery`. |
| `addresses[].firstname` | string | yes | Recipient first name. |
| `addresses[].lastname` | string | yes | Recipient last name. |
| `addresses[].street1` | string | yes | Primary street line for the delivery address. |
| `addresses[].zip` | string | yes | Postal or ZIP code for the delivery address. |
| `addresses[].city` | string | yes | City for the delivery address. |
| `addresses[].country` | string | yes | Delivery country in ISO 3166-1 alpha-2 format. |
| `addresses[].email` | string | yes | Email for the delivery address contact. |
| `addresses[].phone` | string | yes | Phone number for the delivery address contact. Required by the live API. |
| `items[]` | array<object> | yes | One or more order items. |
| `items[].reference` | string | yes | Client item reference. Must match the reference used when quoting. |
| `items[].product` | string | yes | Cloudprinter product reference. |
| `items[].count` | string | yes | Number of copies to produce for this item. |
| `items[].quote` | string | no | Quote hash returned by Get Order Quote for this item. |
| `items[].shippingLevel` | string | no | Preferred shipping level when no quote hash is supplied. |
| `items[].title` | string | no | Optional customer-facing item title. |
| `items[].options[]` | array<object> | no | Optional item options. Cloudprinter expects an array value even when empty. Default: `[]`. |
| `items[].files[]` | array<object> | yes | Files to print for this item. |
| `items[].files[].type` | string | yes | File type expected by the selected product. |
| `items[].files[].url` | string | yes | HTTPS URL where Cloudprinter can download the print file. |
| `items[].files[].md5sum` | string | yes | MD5 checksum used by Cloudprinter to validate the downloaded file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "order": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `order` | string |  |

## Native endpoint

Through the native Cloudprinter.com API, this operation is `POST /cloudcore/1.0/orders/add` (base URL `https://api.cloudprinter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-order.md) for the provider-specific parameters and requirements.

