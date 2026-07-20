# Productive.io: Get Contact Entry

Retrieves a contact entry from your Productive.io account.

```
GET https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/get-contact-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productive.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/get-contact-entry?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/get-contact-entry?${params}`, {
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
| `id` | string | yes | The Productive resource ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "address": "string",
        "billingAddress": "string",
        "billingEmail": "ava@example.com",
        "city": "string",
        "contactableType": "string",
        "country": "string",
        "email": "ava@example.com",
        "name": "Ava Chen",
        "phone": "string",
        "state": "string",
        "type": "string",
        "vat": "string",
        "website": "string",
        "zipcode": "string"
      },
      "id": "string",
      "relationships": {
        "company": {
          "meta": {
            "included": true
          }
        },
        "invoice": {
          "meta": {
            "included": true
          }
        },
        "invoiceTemplate": {
          "meta": {
            "included": true
          }
        },
        "organization": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "person": {
          "meta": {
            "included": true
          }
        },
        "purchaseOrder": {
          "meta": {
            "included": true
          }
        },
        "subsidiary": {
          "meta": {
            "included": true
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.address` | string |  |
| `attributes.billingAddress` | string |  |
| `attributes.billingEmail` | string |  |
| `attributes.city` | string |  |
| `attributes.contactableType` | string |  |
| `attributes.country` | string |  |
| `attributes.email` | string |  |
| `attributes.name` | string |  |
| `attributes.phone` | string |  |
| `attributes.state` | string |  |
| `attributes.type` | string |  |
| `attributes.vat` | string |  |
| `attributes.website` | string |  |
| `attributes.zipcode` | string |  |
| `id` | string |  |
| `relationships.company.meta.included` | boolean |  |
| `relationships.invoice.meta.included` | boolean |  |
| `relationships.invoiceTemplate.meta.included` | boolean |  |
| `relationships.organization.data.id` | string |  |
| `relationships.organization.data.type` | string |  |
| `relationships.person.meta.included` | boolean |  |
| `relationships.purchaseOrder.meta.included` | boolean |  |
| `relationships.subsidiary.meta.included` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Productive.io API, this operation is `GET /contact_entries/{{id}}` (base URL `https://api.productive.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-entry.md) for the provider-specific parameters and requirements.

