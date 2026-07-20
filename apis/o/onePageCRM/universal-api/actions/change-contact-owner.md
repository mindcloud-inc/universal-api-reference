# OnePageCRM: Change Contact Owner

Changes a contact's owner in OnePageCRM.

```
PUT https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/change-contact-owner
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePageCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/change-contact-owner" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "Select a contact",
  "ownerId": "Select a user"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/change-contact-owner', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "Select a contact",
    "ownerId": "Select a user"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | list<string> | yes | Contact ID. Example: `Select a contact`. |
| `ownerId` | list<string> | yes | Owner ID. Example: `Select a user`. |

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

Through the native OnePageCRM API, this operation is `PUT /contacts/:contact_id/change_owner/:owner_id` (base URL `https://app.onepagecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-contact-owner.md) for the provider-specific parameters and requirements.

