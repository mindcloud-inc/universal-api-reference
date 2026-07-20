# OnePageCRM: List Companies

Retrieves companies from OnePageCRM.

```
GET https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePageCRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-companies?${params}`, {
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
| `name` | string | no | Search companies by name Example: `Acme Ltd`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phone` | string | no | Search companies by phone number Example: `+1 555 123 4567`. |
| `letter` | string | no | Return companies whose name begins with the specified letter Example: `A`. |

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
          }
        }
      ],
      "contactsCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "lastTimelineUpdate": "2026-05-07T12:00:00.000Z",
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
| `contactsCount` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `lastTimelineUpdate` | date |  |
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

Through the native OnePageCRM API, this operation is `GET /companies` (base URL `https://app.onepagecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

