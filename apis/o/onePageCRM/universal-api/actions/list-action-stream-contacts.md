# OnePageCRM: List Action Stream Contacts

Retrieves contacts from OnePageCRM prioritized by next action.

```
GET https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-action-stream-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePageCRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-action-stream-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-action-stream-contacts?${params}`, {
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
| `search` | string | no | Search contacts by contact name, company name, or phone number. Example: `Jane Doe`. |
| `email` | string | no | Match contacts by email address. Example: `abc@example.com`. |
| `phone` | string | no | Search contacts by phone number. Example: `3736344458`. |
| `url` | string | no | Search contacts by web address. Example: `https://example.com`. |
| `team` | boolean | no | Include contacts owned by other users. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `letter` | string | no | Match contacts whose last name begins with the specified letter. Example: `A`. |
| `statusId` | string | no | Return contacts of a particular status. Example: `5aaa9b039007ba08c9ebaf0b`. |
| `ownerId` | string | no | Return contacts owned by a specific user. Example: `5aba36b19007ba0f570c9523`. |
| `companyId` | string | no | Return contacts from a specific company. Example: `6se06df9d55673108re84745`. |
| `tag` | string | no | Filter contacts by tag. Example: `VIP`. |
| `filterId` | string | no | Apply a saved contact filter. Example: `5ae9cc2a9007ba5b856c7bb8`. |
| `leadSource` | string | no | Return contacts of a specific lead source. Example: `Referral`. |
| `leadSourceId` | string | no | Return contacts of a specific lead source by ID. Example: `5aec63769007ba365a4e9ba0`. |
| `customFieldId` | string | no | Custom field ID to combine with Custom Field Value. Example: `5afaf6299007ba5c417f0d72`. |
| `customFieldValue` | string | no | Custom field value to combine with Custom Field ID. Example: `Enterprise`. |
| `actionStream` | boolean | no | Only return results that are also in the action stream. |
| `hasActions` | boolean | no | Return owned contacts that have actions for any user. |
| `hasActionsForMe` | boolean | no | Return owned contacts that have actions for the logged user. |
| `pendingDeal` | boolean | no | Only return contacts that have a pending deal. |
| `starred` | boolean | no | Only return starred contacts. |
| `waiting` | boolean | no | Only return contacts where my next action has waiting status. |
| `dateFilter` | list<string> | no | Choose which date field to use with Since or Until. One of: `created_at`, `modified_at`, `updated_at`. |
| `since` | date | no | Return resources added or edited since this date or timestamp. Example: `2018-07-01`. |
| `until` | date | no | Return resources added or edited until this date or timestamp. Example: `2018-07-31`. |
| `modifiedSince` | date | no | Return only resources modified since this date or timestamp. Example: `2018-07-01`. |
| `unmodifiedSince` | date | no | Return only resources unmodified since this date or timestamp. Example: `2018-07-01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {
        "address": {
          "address": {},
          "city": {},
          "countryCode": {},
          "state": {},
          "zipCode": {}
        },
        "contactsCount": 1,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "id": "string",
        "lastTimelineUpdate": "2026-05-07T12:00:00.000Z",
        "modifiedAt": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "phone": "string",
        "photoUrl": "https://example.com",
        "syncedStatusId": {},
        "syncedTags": {},
        "syncingStatus": true,
        "syncingTags": true,
        "url": "https://example.com"
      },
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
        "emails": [
          {
            "type": "ava@example.com",
            "value": "ava@example.com"
          }
        ],
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
        "phones": [
          {
            "type": "string",
            "value": "string"
          }
        ],
        "photoUrl": "https://example.com",
        "starred": true,
        "status": "string",
        "statusId": "string",
        "totalDealsCount": 1,
        "totalPendings": 1,
        "urls": [
          {
            "type": "https://example.com",
            "value": "https://example.com"
          }
        ]
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company.address.address` | object |  |
| `company.address.city` | object |  |
| `company.address.countryCode` | object |  |
| `company.address.state` | object |  |
| `company.address.zipCode` | object |  |
| `company.contactsCount` | number |  |
| `company.createdAt` | date |  |
| `company.description` | string |  |
| `company.id` | string |  |
| `company.lastTimelineUpdate` | date |  |
| `company.modifiedAt` | date |  |
| `company.name` | string |  |
| `company.phone` | string |  |
| `company.photoUrl` | string |  |
| `company.syncedStatusId` | object |  |
| `company.syncedTags` | object |  |
| `company.syncingStatus` | boolean |  |
| `company.syncingTags` | boolean |  |
| `company.url` | string |  |
| `contact.addressList[].address` | string |  |
| `contact.addressList[].city` | string |  |
| `contact.addressList[].countryCode` | string |  |
| `contact.addressList[].state` | string |  |
| `contact.addressList[].type` | string |  |
| `contact.addressList[].zipCode` | string |  |
| `contact.background` | string |  |
| `contact.companyId` | string |  |
| `contact.companyName` | string |  |
| `contact.companySize` | number |  |
| `contact.createdAt` | date |  |
| `contact.emails[].type` | string |  |
| `contact.emails[].value` | string |  |
| `contact.emailSyncAvailable` | boolean |  |
| `contact.emailSyncEnabled` | boolean |  |
| `contact.enhanceable` | boolean |  |
| `contact.firstName` | string |  |
| `contact.googleContactsData` | object |  |
| `contact.id` | string |  |
| `contact.jobTitle` | string |  |
| `contact.lastName` | string |  |
| `contact.lastTimelineUpdate` | date |  |
| `contact.leadSource` | string |  |
| `contact.leadSourceId` | string |  |
| `contact.letter` | string |  |
| `contact.modifiedAt` | date |  |
| `contact.ownerId` | string |  |
| `contact.pendingDeal` | boolean |  |
| `contact.phones[].type` | string |  |
| `contact.phones[].value` | string |  |
| `contact.photoUrl` | string |  |
| `contact.starred` | boolean |  |
| `contact.status` | string |  |
| `contact.statusId` | string |  |
| `contact.totalDealsCount` | number |  |
| `contact.totalPendings` | number |  |
| `contact.urls[].type` | string |  |
| `contact.urls[].value` | string |  |
| `mostUrgentAction.assigneeId` | string |  |
| `mostUrgentAction.contactId` | string |  |
| `mostUrgentAction.createdAt` | date |  |
| `mostUrgentAction.date` | date |  |
| `mostUrgentAction.done` | boolean |  |
| `mostUrgentAction.id` | string |  |
| `mostUrgentAction.modifiedAt` | date |  |
| `mostUrgentAction.status` | string |  |
| `mostUrgentAction.text` | string |  |
| `nextAction.assigneeId` | string |  |
| `nextAction.contactId` | string |  |
| `nextAction.createdAt` | date |  |
| `nextAction.date` | date |  |
| `nextAction.done` | boolean |  |
| `nextAction.id` | string |  |
| `nextAction.modifiedAt` | date |  |
| `nextAction.status` | string |  |
| `nextAction.text` | string |  |
| `nextActions[].assigneeId` | string |  |
| `nextActions[].contactId` | string |  |
| `nextActions[].createdAt` | date |  |
| `nextActions[].date` | date |  |
| `nextActions[].done` | boolean |  |
| `nextActions[].id` | string |  |
| `nextActions[].modifiedAt` | date |  |
| `nextActions[].status` | string |  |
| `nextActions[].text` | string |  |

## Native endpoint

Through the native OnePageCRM API, this operation is `GET /action_stream` (base URL `https://app.onepagecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-action-stream-contacts.md) for the provider-specific parameters and requirements.

