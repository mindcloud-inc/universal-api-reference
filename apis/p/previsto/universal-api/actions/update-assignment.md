# Previsto: Update Assignment

Updates an existing assignment in Previsto.

```
PUT https://connect.mindcloud.co/v1/universal/previsto/latest/actions/update-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Previsto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/previsto/latest/actions/update-assignment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/previsto/latest/actions/update-assignment', {
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
| `id` | string | yes | Previsto assignment ID. |
| `accountId` | string | no | Assigned worker account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "action": "string",
      "address": {
        "apartment": {},
        "city": {},
        "countryCode": "string",
        "postalCode": {},
        "street": {}
      },
      "contactId": "string",
      "contactName": "Ava Chen",
      "createdBy": "string",
      "createdDate": "string",
      "deliveryAddress": {},
      "flagged": true,
      "handledDate": {},
      "id": "string",
      "lastModifiedBy": "string",
      "lastModifiedDate": "string",
      "location": [
        1
      ],
      "locationResolvementStatus": "string",
      "message": {},
      "notifiedOfImpendingWork": true,
      "payingContactId": "string",
      "plan": {
        "affixment": {
          "link": {},
          "state": "string"
        },
        "allDay": true,
        "completionDuePeriod": {},
        "completionDueTime": {},
        "executionTime": "string",
        "indicativeDate": "string",
        "indicativeDateType": "string",
        "mode": "string",
        "serviceWindow": {
          "endTime": "string",
          "startTime": "string"
        },
        "specificStartTime": true
      },
      "remoteOrderId": {},
      "sentState": "string",
      "stateId": "string",
      "status": "string",
      "tasks": [
        {
          "description": "string",
          "duration": 1,
          "message": {},
          "note": {},
          "priorMessage": {},
          "quantity": 1,
          "quantityUnit": "string",
          "reference": "string",
          "unitPrice": 1,
          "workType": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `action` | string |  |
| `address.apartment` | object |  |
| `address.city` | object |  |
| `address.countryCode` | string |  |
| `address.postalCode` | object |  |
| `address.street` | object |  |
| `contactId` | string |  |
| `contactName` | string |  |
| `createdBy` | string |  |
| `createdDate` | string |  |
| `deliveryAddress` | object |  |
| `flagged` | boolean |  |
| `handledDate` | object |  |
| `id` | string |  |
| `lastModifiedBy` | string |  |
| `lastModifiedDate` | string |  |
| `location[]` | number |  |
| `locationResolvementStatus` | string |  |
| `message` | object |  |
| `notifiedOfImpendingWork` | boolean |  |
| `payingContactId` | string |  |
| `plan.affixment.link` | object |  |
| `plan.affixment.state` | string |  |
| `plan.allDay` | boolean |  |
| `plan.completionDuePeriod` | object |  |
| `plan.completionDueTime` | object |  |
| `plan.executionTime` | string |  |
| `plan.indicativeDate` | string |  |
| `plan.indicativeDateType` | string |  |
| `plan.mode` | string |  |
| `plan.serviceWindow.endTime` | string |  |
| `plan.serviceWindow.startTime` | string |  |
| `plan.specificStartTime` | boolean |  |
| `remoteOrderId` | object |  |
| `sentState` | string |  |
| `stateId` | string |  |
| `status` | string |  |
| `tasks[].description` | string |  |
| `tasks[].duration` | number |  |
| `tasks[].message` | object |  |
| `tasks[].note` | object |  |
| `tasks[].priorMessage` | object |  |
| `tasks[].quantity` | number |  |
| `tasks[].quantityUnit` | string |  |
| `tasks[].reference` | string |  |
| `tasks[].unitPrice` | number |  |
| `tasks[].workType` | string |  |

## Native endpoint

Through the native Previsto API, this operation is `PUT /assignments/:id` (base URL `https://api.previsto.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-assignment.md) for the provider-specific parameters and requirements.

