# Syncro: Update Customer

Updates an existing customer in Syncro.

```
PUT https://connect.mindcloud.co/v1/universal/syncro/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/syncro/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The Syncro customer ID. |
| `businessName` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `email` | string | no |  |
| `phone` | string | no |  |
| `mobile` | string | no |  |
| `address` | string | no |  |
| `address2` | string | no |  |
| `city` | string | no |  |
| `state` | string | no |  |
| `zip` | string | no |  |
| `notes` | string | no |  |
| `getSms` | boolean | no |  |
| `optOut` | boolean | no |  |
| `noEmail` | boolean | no |  |
| `getBilling` | boolean | no |  |
| `getMarketing` | boolean | no |  |
| `getReports` | boolean | no |  |
| `refCustomerId` | number | no |  |
| `referredBy` | string | no |  |
| `taxRateId` | number | no |  |
| `notificationEmail` | string | no |  |
| `invoiceCcEmails` | string | no |  |
| `invoiceTermId` | number | no |  |
| `properties` | object | no |  |
| `consent` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customer": {
        "address": "string",
        "businessAndFullName": "Ava Chen",
        "businessName": "Ava Chen",
        "city": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "disabled": true,
        "email": "ava@example.com",
        "firstname": "Ava",
        "fullname": "Ava Chen",
        "getSms": true,
        "id": 1,
        "lastname": "Chen",
        "mobile": "string",
        "noEmail": true,
        "onlineProfileUrl": "https://example.com",
        "optOut": true,
        "phone": "string",
        "properties": {
          "notificationBilling": "string",
          "notificationMarketing": "string",
          "notificationReports": "string"
        },
        "state": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer.address` | string |  |
| `customer.businessAndFullName` | string |  |
| `customer.businessName` | string |  |
| `customer.city` | string |  |
| `customer.createdAt` | date |  |
| `customer.disabled` | boolean |  |
| `customer.email` | string |  |
| `customer.firstname` | string |  |
| `customer.fullname` | string |  |
| `customer.getSms` | boolean |  |
| `customer.id` | number |  |
| `customer.lastname` | string |  |
| `customer.mobile` | string |  |
| `customer.noEmail` | boolean |  |
| `customer.onlineProfileUrl` | string |  |
| `customer.optOut` | boolean |  |
| `customer.phone` | string |  |
| `customer.properties.notificationBilling` | string |  |
| `customer.properties.notificationMarketing` | string |  |
| `customer.properties.notificationReports` | string |  |
| `customer.state` | string |  |
| `customer.updatedAt` | date |  |

## Native endpoint

Through the native Syncro API, this operation is `PUT /customers/:id` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

