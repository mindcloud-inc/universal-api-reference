# Previsto: Update Contact

Updates an existing contact in Previsto.

```
PUT https://connect.mindcloud.co/v1/universal/previsto/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Previsto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/previsto/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/previsto/latest/actions/update-contact', {
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
| `address` | string | no | Street address |
| `city` | string | no | City |
| `countryCode` | string | no | 2-letter country code |
| `id` | string | yes | Previsto contact ID. |
| `postalCode` | string | no | Postal code |
| `name` | string | no | Updated contact name. |
| `email` | string | no | Updated contact email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessKey": "string",
      "accountingMode": {},
      "accountingTime": {},
      "address": "string",
      "appartment": {},
      "archived": true,
      "city": "string",
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
      "postalCode": "string",
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
| `address` | string |  |
| `appartment` | object |  |
| `archived` | boolean |  |
| `city` | string |  |
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
| `postalCode` | string |  |
| `registrationNo` | object |  |
| `remoteId` | object |  |
| `remoteOrderId` | object |  |
| `serviceWindow.endTime` | string |  |
| `serviceWindow.startTime` | string |  |

## Native endpoint

Through the native Previsto API, this operation is `PUT /contacts/:id` (base URL `https://api.previsto.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

