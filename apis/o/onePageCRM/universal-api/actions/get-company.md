# OnePageCRM: Get Company

Retrieves a company from OnePageCRM.

```
GET https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePageCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/get-company?connectionId=$CONNECTION_ID&companyId=Acme%20Inc." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "Acme Inc."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/get-company?${params}`, {
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
| `companyId` | list<string> | yes | ID of the company to retrieve Example: `Acme Inc.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "address": {},
        "city": {},
        "countryCode": {},
        "state": {},
        "zipCode": {}
      },
      "contacts": [
        {
          "contact": {
            "addressList": [
              {
                "address": "string",
                "city": "string",
                "countryCode": "string",
                "state": "string",
                "type": "string",
                "zipCode": "string"
              }
            ],
            "background": "string",
            "companyId": "string",
            "companyName": "Ava Chen",
            "companySize": 1,
            "createdAt": "2026-05-07T12:00:00.000Z",
            "emailSyncAvailable": true,
            "emailSyncEnabled": true,
            "enhanceable": true,
            "firstName": "Ava",
            "googleContactsData": {},
            "id": "string",
            "jobTitle": "string",
            "lastName": "Chen",
            "lastTimelineUpdate": "2026-05-07T12:00:00.000Z",
            "leadSource": "string",
            "leadSourceId": "string",
            "letter": "string",
            "modifiedAt": "2026-05-07T12:00:00.000Z",
            "ownerId": "string",
            "pendingDeal": true,
            "photoUrl": "https://example.com",
            "starred": true,
            "status": "string",
            "statusId": "string",
            "totalDealsCount": 1,
            "totalPendings": 1
          },
          "mostUrgentAction": {
            "assigneeId": "string",
            "contactId": "string",
            "createdAt": "2026-05-07T12:00:00.000Z",
            "date": "2026-05-07T12:00:00.000Z",
            "done": true,
            "id": "string",
            "modifiedAt": "2026-05-07T12:00:00.000Z",
            "status": "string",
            "text": "string"
          },
          "nextAction": {
            "assigneeId": "string",
            "contactId": "string",
            "createdAt": "2026-05-07T12:00:00.000Z",
            "date": "2026-05-07T12:00:00.000Z",
            "done": true,
            "id": "string",
            "modifiedAt": "2026-05-07T12:00:00.000Z",
            "status": "string",
            "text": "string"
          },
          "nextActions": [
            {
              "assigneeId": "string",
              "contactId": "string",
              "createdAt": "2026-05-07T12:00:00.000Z",
              "date": "2026-05-07T12:00:00.000Z",
              "done": true,
              "id": "string",
              "modifiedAt": "2026-05-07T12:00:00.000Z",
              "status": "string",
              "text": "string"
            }
          ]
        }
      ],
      "contactsCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "lastTimelineUpdate": "2026-05-07T12:00:00.000Z",
      "linkedContactsCount": 1,
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "pendingDealsCount": 1,
      "phone": "string",
      "photoUrl": "https://example.com",
      "syncedStatusId": {},
      "syncedTags": {},
      "syncingStatus": true,
      "syncingTags": true,
      "totalPendingAmount": 1,
      "totalWonAmount": 1,
      "url": "https://example.com",
      "wonDealsCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.address` | object |  |
| `address.city` | object |  |
| `address.countryCode` | object |  |
| `address.state` | object |  |
| `address.zipCode` | object |  |
| `contacts[].contact.addressList[].address` | string |  |
| `contacts[].contact.addressList[].city` | string |  |
| `contacts[].contact.addressList[].countryCode` | string |  |
| `contacts[].contact.addressList[].state` | string |  |
| `contacts[].contact.addressList[].type` | string |  |
| `contacts[].contact.addressList[].zipCode` | string |  |
| `contacts[].contact.background` | string |  |
| `contacts[].contact.companyId` | string |  |
| `contacts[].contact.companyName` | string |  |
| `contacts[].contact.companySize` | number |  |
| `contacts[].contact.createdAt` | date |  |
| `contacts[].contact.emailSyncAvailable` | boolean |  |
| `contacts[].contact.emailSyncEnabled` | boolean |  |
| `contacts[].contact.enhanceable` | boolean |  |
| `contacts[].contact.firstName` | string |  |
| `contacts[].contact.googleContactsData` | object |  |
| `contacts[].contact.id` | string |  |
| `contacts[].contact.jobTitle` | string |  |
| `contacts[].contact.lastName` | string |  |
| `contacts[].contact.lastTimelineUpdate` | date |  |
| `contacts[].contact.leadSource` | string |  |
| `contacts[].contact.leadSourceId` | string |  |
| `contacts[].contact.letter` | string |  |
| `contacts[].contact.modifiedAt` | date |  |
| `contacts[].contact.ownerId` | string |  |
| `contacts[].contact.pendingDeal` | boolean |  |
| `contacts[].contact.photoUrl` | string |  |
| `contacts[].contact.starred` | boolean |  |
| `contacts[].contact.status` | string |  |
| `contacts[].contact.statusId` | string |  |
| `contacts[].contact.totalDealsCount` | number |  |
| `contacts[].contact.totalPendings` | number |  |
| `contacts[].mostUrgentAction.assigneeId` | string |  |
| `contacts[].mostUrgentAction.contactId` | string |  |
| `contacts[].mostUrgentAction.createdAt` | date |  |
| `contacts[].mostUrgentAction.date` | date |  |
| `contacts[].mostUrgentAction.done` | boolean |  |
| `contacts[].mostUrgentAction.id` | string |  |
| `contacts[].mostUrgentAction.modifiedAt` | date |  |
| `contacts[].mostUrgentAction.status` | string |  |
| `contacts[].mostUrgentAction.text` | string |  |
| `contacts[].nextAction.assigneeId` | string |  |
| `contacts[].nextAction.contactId` | string |  |
| `contacts[].nextAction.createdAt` | date |  |
| `contacts[].nextAction.date` | date |  |
| `contacts[].nextAction.done` | boolean |  |
| `contacts[].nextAction.id` | string |  |
| `contacts[].nextAction.modifiedAt` | date |  |
| `contacts[].nextAction.status` | string |  |
| `contacts[].nextAction.text` | string |  |
| `contacts[].nextActions[].assigneeId` | string |  |
| `contacts[].nextActions[].contactId` | string |  |
| `contacts[].nextActions[].createdAt` | date |  |
| `contacts[].nextActions[].date` | date |  |
| `contacts[].nextActions[].done` | boolean |  |
| `contacts[].nextActions[].id` | string |  |
| `contacts[].nextActions[].modifiedAt` | date |  |
| `contacts[].nextActions[].status` | string |  |
| `contacts[].nextActions[].text` | string |  |
| `contactsCount` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `lastTimelineUpdate` | date |  |
| `linkedContactsCount` | number |  |
| `modifiedAt` | date |  |
| `name` | string |  |
| `pendingDealsCount` | number |  |
| `phone` | string |  |
| `photoUrl` | string |  |
| `syncedStatusId` | object |  |
| `syncedTags` | object |  |
| `syncingStatus` | boolean |  |
| `syncingTags` | boolean |  |
| `totalPendingAmount` | number |  |
| `totalWonAmount` | number |  |
| `url` | string |  |
| `wonDealsCount` | number |  |

## Native endpoint

Through the native OnePageCRM API, this operation is `GET /companies/:company_id` (base URL `https://app.onepagecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

