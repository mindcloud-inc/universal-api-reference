# TrackMage: Update Order

Updates an existing order in TrackMage.

```
PUT https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/update-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackMage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/update-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/update-order', {
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
| `id` | string | yes | Resource identifier |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subtotal` | string | no | The current subtotal price of the order in the store currency. Default value is **0** |
| `total` | string | no | The current total price of the order in the store currency. Default value is **0** |
| `currency` | string | no | A three-letter currency code. Default value is **USD** |
| `orderStatus.code` | string | no | A unique status code. This field is required. |
| `orderStatus.title` | string | no | A status name. This field is optional. |
| `orderStatus.description` | string | no |  |
| `email` | string | no | Customer email address. |
| `phoneNumber` | string | no | Customer phone number. |
| `shipments[]` | array<string> | no | List of [shipment](/docs/Shipment/shipment.html) references that belong to the order. |
| `shippingAddress.addressLine1` | string | no | The street address. This field is optional. |
| `shippingAddress.addressLine2` | string | no | An optional additional field for the street address. This field is optional. |
| `shippingAddress.city` | string | no | The city, town, or village. This field is optional. |
| `shippingAddress.company` | string | no | The company of the person associated with the address. This field is optional. |
| `shippingAddress.country` | string | no | The name of the country. This field is optional. |
| `shippingAddress.countryIso2` | string | no | The two-letter country code. This field is optional. |
| `shippingAddress.firstName` | string | no | The first name of the person associated with the address. This field is optional. |
| `shippingAddress.lastName` | string | no | The last name of the person associated with the address. This field is optional. |
| `shippingAddress.postcode` | string | no | The postal code (zip, postcode, Eircode, …). This field is optional. |
| `shippingAddress.state` | string | no | The name of the region (province, state, prefecture, …). This field is optional. |
| `billingAddress.addressLine1` | string | no | The street address. This field is optional. |
| `billingAddress.addressLine2` | string | no | An optional additional field for the street address. This field is optional. |
| `billingAddress.city` | string | no | The city, town, or village. This field is optional. |
| `billingAddress.company` | string | no | The company of the person associated with the address. This field is optional. |
| `billingAddress.country` | string | no | The name of the country. This field is optional. |
| `billingAddress.countryIso2` | string | no | The two-letter country code. This field is optional. |
| `billingAddress.firstName` | string | no | The first name of the person associated with the address. This field is optional. |
| `billingAddress.lastName` | string | no | The last name of the person associated with the address. This field is optional. |
| `billingAddress.postcode` | string | no | The postal code (zip, postcode, Eircode, …). This field is optional. |
| `billingAddress.state` | string | no | The name of the region (province, state, prefecture, …). This field is optional. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingAddress": {
        "addressLine1": "string",
        "addressLine2": "string",
        "city": "string",
        "company": "string",
        "country": "string",
        "countryIso2": "string",
        "firstName": "Ava",
        "lastName": "Chen",
        "postcode": "string",
        "state": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "email": "ava@example.com",
      "externalSourceIntegration": "string",
      "externalSourceIntegrationType": "string",
      "externalSourceSyncId": "string",
      "externalSourceUrl": "https://example.com",
      "fulfillmentStatus": "string",
      "id": "string",
      "orderNumber": "string",
      "orderStatus": {
        "code": "string",
        "description": "string",
        "id": "string",
        "title": "string"
      },
      "orderType": "string",
      "phoneNumber": "string",
      "readonly": true,
      "shipments": [
        "string"
      ],
      "shipmentsWithoutTrackingCount": 1,
      "shippingAddress": {
        "addressLine1": "string",
        "addressLine2": "string",
        "city": "string",
        "company": "string",
        "country": "string",
        "countryIso2": "string",
        "firstName": "Ava",
        "lastName": "Chen",
        "postcode": "string",
        "state": "string"
      },
      "subtotal": "string",
      "total": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingAddress` | object |  |
| `billingAddress.addressLine1` | string |  |
| `billingAddress.addressLine2` | string |  |
| `billingAddress.city` | string |  |
| `billingAddress.company` | string |  |
| `billingAddress.country` | string |  |
| `billingAddress.countryIso2` | string |  |
| `billingAddress.firstName` | string |  |
| `billingAddress.lastName` | string |  |
| `billingAddress.postcode` | string |  |
| `billingAddress.state` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `email` | string |  |
| `externalSourceIntegration` | string |  |
| `externalSourceIntegrationType` | string |  |
| `externalSourceSyncId` | string |  |
| `externalSourceUrl` | string |  |
| `fulfillmentStatus` | string |  |
| `id` | string |  |
| `orderNumber` | string |  |
| `orderStatus` | object |  |
| `orderStatus.code` | string |  |
| `orderStatus.description` | string |  |
| `orderStatus.id` | string |  |
| `orderStatus.title` | string |  |
| `orderType` | string |  |
| `phoneNumber` | string |  |
| `readonly` | boolean |  |
| `shipments` | array<string> |  |
| `shipmentsWithoutTrackingCount` | number |  |
| `shippingAddress` | object |  |
| `shippingAddress.addressLine1` | string |  |
| `shippingAddress.addressLine2` | string |  |
| `shippingAddress.city` | string |  |
| `shippingAddress.company` | string |  |
| `shippingAddress.country` | string |  |
| `shippingAddress.countryIso2` | string |  |
| `shippingAddress.firstName` | string |  |
| `shippingAddress.lastName` | string |  |
| `shippingAddress.postcode` | string |  |
| `shippingAddress.state` | string |  |
| `subtotal` | string |  |
| `total` | string |  |
| `updatedAt` | date |  |
| `workspace` | string |  |

## Native endpoint

Through the native TrackMage API, this operation is `PUT /orders/{id}` (base URL `https://api.trackmage.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order.md) for the provider-specific parameters and requirements.

