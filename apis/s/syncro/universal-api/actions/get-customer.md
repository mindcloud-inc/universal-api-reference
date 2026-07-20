# Syncro: Get Customer

Retrieves a customer from Syncro by ID.

```
GET https://connect.mindcloud.co/v1/universal/syncro/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/get-customer?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syncro/latest/actions/get-customer?${params}`, {
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
| `id` | number | yes | The Syncro customer ID. |

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
        "contacts": [
          {
            "accountId": 1,
            "customerId": 1,
            "email": "ava@example.com",
            "id": 1,
            "name": "Ava Chen",
            "phone": "string"
          }
        ],
        "createdAt": "2026-05-07T12:00:00.000Z",
        "disabled": true,
        "email": "ava@example.com",
        "firstname": "Ava",
        "fullname": "Ava Chen",
        "getSms": true,
        "id": 1,
        "lastname": "Chen",
        "latitude": 1,
        "longitude": 1,
        "mobile": "string",
        "noEmail": true,
        "onlineProfileUrl": "https://example.com",
        "optOut": true,
        "phone": "string",
        "phones": [
          {
            "customerId": 1,
            "id": 1,
            "label": "string",
            "number": "string"
          }
        ],
        "properties": {
          "notificationBilling": "string",
          "notificationMarketing": "string",
          "notificationReports": "string"
        },
        "sinceUpdatedAt": "2026-05-07T12:00:00.000Z",
        "state": "string",
        "ticketLinks": [
          {
            "id": 1,
            "number": 1,
            "status": "https://example.com",
            "subject": "https://example.com"
          }
        ],
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
| `customer.contacts[].accountId` | number |  |
| `customer.contacts[].customerId` | number |  |
| `customer.contacts[].email` | string |  |
| `customer.contacts[].id` | number |  |
| `customer.contacts[].name` | string |  |
| `customer.contacts[].phone` | string |  |
| `customer.createdAt` | date |  |
| `customer.disabled` | boolean |  |
| `customer.email` | string |  |
| `customer.firstname` | string |  |
| `customer.fullname` | string |  |
| `customer.getSms` | boolean |  |
| `customer.id` | number |  |
| `customer.lastname` | string |  |
| `customer.latitude` | number |  |
| `customer.longitude` | number |  |
| `customer.mobile` | string |  |
| `customer.noEmail` | boolean |  |
| `customer.onlineProfileUrl` | string |  |
| `customer.optOut` | boolean |  |
| `customer.phone` | string |  |
| `customer.phones[].customerId` | number |  |
| `customer.phones[].id` | number |  |
| `customer.phones[].label` | string |  |
| `customer.phones[].number` | string |  |
| `customer.properties.notificationBilling` | string |  |
| `customer.properties.notificationMarketing` | string |  |
| `customer.properties.notificationReports` | string |  |
| `customer.sinceUpdatedAt` | date |  |
| `customer.state` | string |  |
| `customer.ticketLinks[].id` | number |  |
| `customer.ticketLinks[].number` | number |  |
| `customer.ticketLinks[].status` | string |  |
| `customer.ticketLinks[].subject` | string |  |
| `customer.updatedAt` | date |  |

## Native endpoint

Through the native Syncro API, this operation is `GET /customers/:id` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

