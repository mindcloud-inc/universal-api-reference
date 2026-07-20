# Booqable: Update Customer

Updates an existing customer in Booqable.

```
PUT https://connect.mindcloud.co/v1/universal/booqable/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Booqable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/booqable/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/booqable/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Customer ID. |
| `fields.customers` | string | no | Comma-separated customer fields to include instead of the default field set. |
| `include` | string | no | Comma-separated relationships to sideload. |
| `data.attributes.name` | string | no | Person or company name. |
| `data.attributes.email` | string | no | Email address used for communication. |
| `data.attributes.legalType` | string | no | Whether the customer is a person or commercial entity. |
| `data.attributes.depositType` | string | no | Default deposit type for new orders. |
| `data.attributes.depositValue` | number | no | Deposit value used with the selected deposit type. |
| `data.attributes.discountPercentage` | number | no | Default discount applied to new orders for this customer. |
| `data.attributes.emailMarketingConsented` | boolean | no | Whether the customer has consented to receive email marketing. |
| `data.attributes.mergeSuggestionCustomerId` | string | no | Customer this record may duplicate. |
| `data.attributes.stripeId` | string | no | Stripe customer ID. |
| `data.attributes.tagList[]` | array<string> | no | Case-insensitive customer tags. |
| `data.attributes.taxRegionId` | string | no | Tax region for new orders for this customer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "archived": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "depositType": "string",
        "depositValue": 1,
        "discountPercentage": 1,
        "email": "ava@example.com",
        "legalType": "string",
        "name": "Ava Chen",
        "number": 1,
        "orderCount": 1,
        "properties": {},
        "tagList": [
          "string"
        ],
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.archived` | boolean | Whether the customer is archived. |
| `attributes.createdAt` | date | When the customer was created. |
| `attributes.depositType` | string | Default deposit type. |
| `attributes.depositValue` | number | Default deposit value. |
| `attributes.discountPercentage` | number | Default discount percentage. |
| `attributes.email` | string | Customer email address. |
| `attributes.legalType` | string | Customer legal type. |
| `attributes.name` | string | Customer name. |
| `attributes.number` | number | Customer number. |
| `attributes.orderCount` | number | Number of orders. |
| `attributes.properties` | object | Custom properties. |
| `attributes.tagList` | array<string> | Customer tags. |
| `attributes.updatedAt` | date | When the customer was last updated. |
| `id` | string | Customer ID. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Booqable API, this operation is `PUT /customers/:id` (base URL `https://mindcloud.booqable.com/api/4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

