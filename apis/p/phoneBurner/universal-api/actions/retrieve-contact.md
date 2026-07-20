# PhoneBurner: Retrieve Contact

Retrieves a specific contact from PhoneBurner.

```
GET https://connect.mindcloud.co/v1/universal/phoneBurner/latest/actions/retrieve-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhoneBurner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phoneBurner/latest/actions/retrieve-contact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phoneBurner/latest/actions/retrieve-contact?${params}`, {
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
| `contactId` | string | no | The PhoneBurner contact id. |

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

Through the native PhoneBurner API, this operation is `GET rest/1/contacts/{{contactId}}` (base URL `https://www.phoneburner.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-contact.md) for the provider-specific parameters and requirements.

