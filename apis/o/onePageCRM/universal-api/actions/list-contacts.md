# OnePageCRM: List Contacts

Retrieves contacts from OnePageCRM.

```
GET https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePageCRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-contacts?${params}`, {
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
| `search` | string | no | Search contacts by contact name, company name, or phone number. Example: `Acme`. |
| `phone` | string | no | Search contacts by phone number. Example: `+14155550123`. |
| `url` | string | no | Search contacts by web address. Example: `example.com`. |
| `starred` | boolean | no | Only return contacts who are starred. |
| `email` | string | no | Return contacts whose email matches the provided value. Example: `alex@example.com`. |
| `letter` | string | no | Return contacts whose last name begins with the specified letter. Example: `A`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `team` | boolean | no | Include contacts owned by other users. |
| `actionStream` | boolean | no | Only return results that are also in the action stream. |
| `hasActions` | boolean | no | Only return contacts owned by the logged user that have actions for any user. |
| `hasActionsForMe` | boolean | no | Only return contacts owned by the logged user that have actions for the logged user. |
| `hasActionsToday` | boolean | no | Only return contacts owned by the logged user that have actions today for the logged user. |
| `pendingDeal` | boolean | no | Only return contacts who have a pending deal. |
| `waiting` | boolean | no | Only return contacts, for whom the logged user has a next action, of status waiting. |
| `customFieldId` | string | no | Filter contacts by custom field value. Use with Custom Field Value. |
| `customFieldValue` | string | no | Filter contacts by custom field value. Use with Custom Field ID. |
| `leadSource` | string | no | Return contacts of a specific lead source. Use either Lead Source or Lead Source ID. |
| `leadSourceId` | list<string> | no | Return contacts of a specific lead source. Use either Lead Source or Lead Source ID. Example: `Select a lead source`. |
| `statusId` | list<string> | no | Return contacts of a particular status. Example: `Select a status`. |
| `notLinkedWith` | string | no | Only return contacts who are not linked to a particular company ID. |
| `ownerId` | list<string> | no | Return contacts owned by a specific user. Example: `Select a user`. |
| `companyId` | string | no | Return contacts from a specific company. Use only one of Company ID, Tag, or Filter ID. |
| `tag` | string | no | Filter contacts by tag. Use only one of Company ID, Tag, or Filter ID. |
| `filterId` | string | no | Apply a filter to contact listing. Use only one of Company ID, Tag, or Filter ID. |
| `dateFilter` | list<string> | no | Choose which date field to use with Since and Until. One of: `created_at`, `modified_at`, `updated_at`. Example: `created_at`. |
| `since` | date | no | Start of the date range to filter resources that were added or edited. Example: `2026-03-01`. |
| `until` | date | no | End of the date range to filter resources that were added or edited. Example: `2026-03-10`. |
| `modifiedSince` | date | no | Return only resources that were modified since the specified time. |
| `unmodifiedSince` | date | no | Return only resources that were unmodified since the specified time. |

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
| `contact.photoUrl` | string |  |
| `contact.starred` | boolean |  |
| `contact.status` | string |  |
| `contact.statusId` | string |  |
| `contact.totalDealsCount` | number |  |
| `contact.totalPendings` | number |  |
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

Through the native OnePageCRM API, this operation is `GET /contacts` (base URL `https://app.onepagecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

