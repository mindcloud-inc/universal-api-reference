# PhoneBurner: List Contacts

Retrieves a list of contacts from PhoneBurner.

```
GET https://connect.mindcloud.co/v1/universal/phoneBurner/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhoneBurner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phoneBurner/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phoneBurner/latest/actions/list-contacts?${params}`, {
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
| `email_address` | string | no | Optional email address filter. |
| `page` | string | no | Page number to fetch. |
| `page_size` | string | no | Number of contacts to fetch per page. |

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

Through the native PhoneBurner API, this operation is `GET rest/1/contacts` (base URL `https://www.phoneburner.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

