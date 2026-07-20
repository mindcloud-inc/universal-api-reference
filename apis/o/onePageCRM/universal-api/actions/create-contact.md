# OnePageCRM: Create Contact

Creates a new contact in OnePageCRM.

```
POST https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePageCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | no | First name of the contact. Example: `Joe`. |
| `lastName` | string | no | Last name of the contact. Example: `Bloggs`. |
| `companyName` | string | no | Name of the company the contact belongs to. Example: `Acme Inc.`. |
| `emails[]` | array<object> | no | Email addresses associated with the contact. |
| `phones[]` | array<object> | no | Phone numbers associated with the contact. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobTitle` | string | no | Job title of the contact. |
| `title` | string | no | The title of the contact. |
| `companyId` | string | no | ID of the company the contact belongs to. |
| `statusId` | list<string> | no | ID of the contact status. Example: `Select a status`. |
| `leadSourceId` | list<string> | no | ID of the lead source. Example: `Select a lead source`. |
| `ownerId` | list<string> | no | ID of the user who owns the contact. Example: `Select a user`. |
| `tags[]` | array<string> | no | Tags applied to the contact. |
| `starred` | boolean | no | Whether the contact is starred. |
| `background` | string | no | Background information about the contact. |
| `urls[]` | array<object> | no | URLs associated with the contact. |
| `addressList[]` | array<object> | no | Addresses associated with the contact. |
| `customFields[]` | array<object> | no | Extra user-configurable contact fields. |

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
| `contactsCount` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `lastTimelineUpdate` | date |  |
| `modifiedAt` | date |  |
| `name` | string |  |
| `phone` | string |  |
| `photoUrl` | string |  |
| `syncedStatusId` | object |  |
| `syncedTags` | object |  |
| `syncingStatus` | boolean |  |
| `syncingTags` | boolean |  |
| `url` | string |  |

## Native endpoint

Through the native OnePageCRM API, this operation is `POST /contacts` (base URL `https://app.onepagecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

