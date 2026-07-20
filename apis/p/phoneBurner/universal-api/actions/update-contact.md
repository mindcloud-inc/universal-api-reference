# PhoneBurner: Update Contact

Updates an existing contact in PhoneBurner.

```
PUT https://connect.mindcloud.co/v1/universal/phoneBurner/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhoneBurner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/phoneBurner/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/phoneBurner/latest/actions/update-contact', {
  method: 'PUT',
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
| `contactId` | string | no | The PhoneBurner contact id. |
| `email` | string | no | Updated email address. |
| `first_name` | string | no | Updated first name. |
| `last_name` | string | no | Updated last name. |
| `notes` | string | no | Updated notes. |
| `phone` | string | no | Updated phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": "string",
      "category": {},
      "contactOwnerId": "string",
      "contactUserId": "string",
      "dateAdded": "string",
      "dateUpdated": "string",
      "description": "string",
      "firstName": "Ava",
      "lastName": "Chen",
      "locationName": "Ava Chen",
      "notes": {},
      "ownerId": "string",
      "primaryEmail": {},
      "primaryPhone": {},
      "rawPhone": "string",
      "region": "string",
      "removed": "string",
      "timeZone": "string",
      "totalCalls": "string",
      "trashed": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | string |  |
| `category` | object |  |
| `contactOwnerId` | string |  |
| `contactUserId` | string |  |
| `dateAdded` | string |  |
| `dateUpdated` | string |  |
| `description` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `locationName` | string |  |
| `notes` | object |  |
| `ownerId` | string |  |
| `primaryEmail` | object |  |
| `primaryPhone` | object |  |
| `rawPhone` | string |  |
| `region` | string |  |
| `removed` | string |  |
| `timeZone` | string |  |
| `totalCalls` | string |  |
| `trashed` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native PhoneBurner API, this operation is `PUT rest/1/contacts/{{contactId}}` (base URL `https://www.phoneburner.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

