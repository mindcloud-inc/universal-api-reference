# TrackMage: Get Order

Retrieves an order from your TrackMage account.

```
GET https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackMage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/get-order?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/get-order?${params}`, {
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
| `id` | string | yes | Resource identifier |

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

Through the native TrackMage API, this operation is `GET /orders/{id}` (base URL `https://api.trackmage.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

