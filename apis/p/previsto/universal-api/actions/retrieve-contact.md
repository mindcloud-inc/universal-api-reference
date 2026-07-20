# Previsto: Retrieve Contact

Retrieves a contact from Previsto.

```
GET https://connect.mindcloud.co/v1/universal/previsto/latest/actions/retrieve-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Previsto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/previsto/latest/actions/retrieve-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/previsto/latest/actions/retrieve-contact?${params}`, {
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
| `id` | string | yes | Previsto contact ID. |

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

Through the native Previsto API, this operation is `GET /contacts/:id` (base URL `https://api.previsto.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-contact.md) for the provider-specific parameters and requirements.

