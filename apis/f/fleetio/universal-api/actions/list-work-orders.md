# Fleetio: List Work Orders

Retrieves a list of work orders from Fleetio.

```
GET https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-work-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-work-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-work-orders?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "commentsCount": 1,
      "completedAt": {},
      "contact": {
        "defaultImageUrl": {},
        "email": "ava@example.com",
        "employee": true,
        "employeeNumber": {},
        "groupId": 1,
        "id": 1,
        "name": "Ava Chen"
      },
      "contactId": 1,
      "createdAt": "string",
      "createdById": 1,
      "customFields": {
        "connectedTo": "string"
      },
      "description": "string",
      "documentsCount": 1,
      "durationInSeconds": {},
      "endingMeterSameAsStart": true,
      "expectedCompletedAt": {},
      "id": 1,
      "imagesCount": 1,
      "invoiceNumber": {},
      "issuedAt": "string",
      "issuedById": 1,
      "issues": [
        {
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "laborTimeInSeconds": {},
      "number": "string",
      "purchaseOrderNumber": {},
      "scheduledAt": {},
      "startedAt": {},
      "state": "string",
      "updatedAt": "string",
      "vehicle": {
        "color": {},
        "defaultImageUrlSmall": {},
        "id": 1,
        "licensePlate": "string",
        "make": "string",
        "model": "string",
        "name": "Ava Chen",
        "registrationExpirationMonth": 1,
        "registrationState": {},
        "trim": {},
        "vin": "string",
        "year": 1
      },
      "vehicleId": 1,
      "vendor": {},
      "vendorId": {},
      "vmrsRepairPriorityClass": {},
      "workOrderStatusColor": "string",
      "workOrderStatusId": 1,
      "workOrderStatusName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentsCount` | number |  |
| `completedAt` | object |  |
| `contact.defaultImageUrl` | object |  |
| `contact.email` | string |  |
| `contact.employee` | boolean |  |
| `contact.employeeNumber` | object |  |
| `contact.groupId` | number |  |
| `contact.id` | number |  |
| `contact.name` | string |  |
| `contactId` | number |  |
| `createdAt` | string |  |
| `createdById` | number |  |
| `customFields.connectedTo` | string |  |
| `description` | string |  |
| `documentsCount` | number |  |
| `durationInSeconds` | object |  |
| `endingMeterSameAsStart` | boolean |  |
| `expectedCompletedAt` | object |  |
| `id` | number |  |
| `imagesCount` | number |  |
| `invoiceNumber` | object |  |
| `issuedAt` | string |  |
| `issuedById` | number |  |
| `issues[].id` | number |  |
| `issues[].name` | string |  |
| `laborTimeInSeconds` | object |  |
| `number` | string |  |
| `purchaseOrderNumber` | object |  |
| `scheduledAt` | object |  |
| `startedAt` | object |  |
| `state` | string |  |
| `updatedAt` | string |  |
| `vehicle.color` | object |  |
| `vehicle.defaultImageUrlSmall` | object |  |
| `vehicle.id` | number |  |
| `vehicle.licensePlate` | string |  |
| `vehicle.make` | string |  |
| `vehicle.model` | string |  |
| `vehicle.name` | string |  |
| `vehicle.registrationExpirationMonth` | number |  |
| `vehicle.registrationState` | object |  |
| `vehicle.trim` | object |  |
| `vehicle.vin` | string |  |
| `vehicle.year` | number |  |
| `vehicleId` | number |  |
| `vendor` | object |  |
| `vendorId` | object |  |
| `vmrsRepairPriorityClass` | object |  |
| `workOrderStatusColor` | string |  |
| `workOrderStatusId` | number |  |
| `workOrderStatusName` | string |  |

## Native endpoint

Through the native Fleetio API, this operation is `GET work_orders` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-work-orders.md) for the provider-specific parameters and requirements.

