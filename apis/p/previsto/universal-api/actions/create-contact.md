# Previsto: Create Contact

Creates a new contact in Previsto.

```
POST https://connect.mindcloud.co/v1/universal/previsto/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Previsto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/previsto/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/previsto/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no | Street address |
| `city` | string | no | City |
| `countryCode` | string | no | 2-letter country code |
| `name` | string | yes | Contact name. |
| `postalCode` | string | no | Postal code |
| `email` | string | no | Contact email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessKey": "string",
      "accountingMode": {},
      "accountingTime": {},
      "address": {},
      "appartment": {},
      "archived": true,
      "city": {},
      "countryCode": "string",
      "createdBy": "string",
      "createdDate": "string",
      "customer": true,
      "ean": {},
      "email": "ava@example.com",
      "id": "string",
      "invoiceDelivery": {},
      "lastModifiedBy": "string",
      "lastModifiedDate": "string",
      "location": [
        1
      ],
      "name": "Ava Chen",
      "note": {},
      "notificationDeliveryMethods": {},
      "notificationEvents": {},
      "notifyBeforeWork": true,
      "number": {},
      "onHold": true,
      "payingContactId": {},
      "phone": {},
      "planningGroupBinderId": {},
      "postalCode": {},
      "registrationNo": {},
      "remoteId": {},
      "remoteOrderId": {},
      "serviceWindow": {
        "endTime": "string",
        "startTime": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessKey` | string |  |
| `accountingMode` | object |  |
| `accountingTime` | object |  |
| `address` | object |  |
| `appartment` | object |  |
| `archived` | boolean |  |
| `city` | object |  |
| `countryCode` | string |  |
| `createdBy` | string |  |
| `createdDate` | string |  |
| `customer` | boolean |  |
| `ean` | object |  |
| `email` | string |  |
| `id` | string |  |
| `invoiceDelivery` | object |  |
| `lastModifiedBy` | string |  |
| `lastModifiedDate` | string |  |
| `location[]` | number |  |
| `name` | string |  |
| `note` | object |  |
| `notificationDeliveryMethods` | object |  |
| `notificationEvents` | object |  |
| `notifyBeforeWork` | boolean |  |
| `number` | object |  |
| `onHold` | boolean |  |
| `payingContactId` | object |  |
| `phone` | object |  |
| `planningGroupBinderId` | object |  |
| `postalCode` | object |  |
| `registrationNo` | object |  |
| `remoteId` | object |  |
| `remoteOrderId` | object |  |
| `serviceWindow.endTime` | string |  |
| `serviceWindow.startTime` | string |  |

## Native endpoint

Through the native Previsto API, this operation is `POST /contacts` (base URL `https://api.previsto.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

