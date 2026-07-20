# Big Cartel: Get All Orders

Retrieves orders from Big Cartel.

```
GET https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/get-all-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Big Cartel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/get-all-orders?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigCartel/latest/actions/get-all-orders?${params}`, {
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
| `accountId` | number | yes | The Big Cartel account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "completedAt": "2026-05-07T12:00:00.000Z",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "customerEmail": "ava@example.com",
        "customerFirstName": "Ava",
        "customerLastName": "Chen",
        "customerNote": "string",
        "customerOptedInToMarketing": true,
        "customerPhoneNumber": "string",
        "discountTotal": "string",
        "itemCount": 1,
        "itemTotal": "string",
        "paymentStatus": "string",
        "shippingAddress1": "string",
        "shippingAddress2": "string",
        "shippingCity": "string",
        "shippingCountryId": "string",
        "shippingCountryName": "Ava Chen",
        "shippingLatitude": 1,
        "shippingLongitude": 1,
        "shippingState": "string",
        "shippingStatus": "string",
        "shippingTotal": "string",
        "shippingZip": "string",
        "taxTotal": "string",
        "total": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "links": {
        "last": "https://example.com",
        "next": "https://example.com",
        "self": "https://example.com"
      },
      "meta": {
        "count": "string"
      },
      "relationships": {
        "adjustments": {
          "data": [
            {}
          ]
        },
        "currency": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "events": {
          "data": [
            {}
          ]
        },
        "items": {
          "data": [
            {}
          ]
        },
        "shippingCountry": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "transactions": {
          "data": [
            {}
          ]
        },
        "warnings": {
          "data": [
            {}
          ]
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
| `attributes.completedAt` | date |  |
| `attributes.createdAt` | date |  |
| `attributes.customerEmail` | string |  |
| `attributes.customerFirstName` | string |  |
| `attributes.customerLastName` | string |  |
| `attributes.customerNote` | string |  |
| `attributes.customerOptedInToMarketing` | boolean |  |
| `attributes.customerPhoneNumber` | string |  |
| `attributes.discountTotal` | string |  |
| `attributes.itemCount` | number |  |
| `attributes.itemTotal` | string |  |
| `attributes.paymentStatus` | string |  |
| `attributes.shippingAddress1` | string |  |
| `attributes.shippingAddress2` | string |  |
| `attributes.shippingCity` | string |  |
| `attributes.shippingCountryId` | string |  |
| `attributes.shippingCountryName` | string |  |
| `attributes.shippingLatitude` | number |  |
| `attributes.shippingLongitude` | number |  |
| `attributes.shippingState` | string |  |
| `attributes.shippingStatus` | string |  |
| `attributes.shippingTotal` | string |  |
| `attributes.shippingZip` | string |  |
| `attributes.taxTotal` | string |  |
| `attributes.total` | string |  |
| `attributes.updatedAt` | date |  |
| `id` | string |  |
| `links.last` | string |  |
| `links.next` | string |  |
| `links.self` | string |  |
| `meta.count` | string |  |
| `relationships.adjustments.data` | array<object> |  |
| `relationships.currency.data.id` | string |  |
| `relationships.currency.data.type` | string |  |
| `relationships.events.data` | array<object> |  |
| `relationships.items.data` | array<object> |  |
| `relationships.shippingCountry.data.id` | string |  |
| `relationships.shippingCountry.data.type` | string |  |
| `relationships.transactions.data` | array<object> |  |
| `relationships.warnings.data` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Big Cartel API, this operation is `GET /v1/accounts/[:account-id]/orders` (base URL `https://api.bigcartel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-orders.md) for the provider-specific parameters and requirements.

