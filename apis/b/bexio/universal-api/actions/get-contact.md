# Bexio: Get Contact

Retrieves a contact from Bexio.

```
GET https://connect.mindcloud.co/v1/universal/bexio/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bexio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bexio/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bexio/latest/actions/get-contact?${params}`, {
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
| `contactId` | number | yes | The ID of the contact. Example: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `showArchived` | boolean | no | Show archived elements only. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "addressAddition": {},
      "birthday": "2026-05-07T12:00:00.000Z",
      "city": "string",
      "contactBranchIds": {},
      "contactGroupIds": "string",
      "contactTypeId": 1,
      "countryId": 1,
      "fax": "string",
      "houseNumber": "string",
      "id": 1,
      "isLead": true,
      "languageId": {},
      "mail": {},
      "mailSecond": {},
      "name1": "Ava Chen",
      "name2": "Ava Chen",
      "nr": "string",
      "ownerId": 1,
      "phoneFixed": {},
      "phoneFixedSecond": {},
      "phoneMobile": "string",
      "postcode": "string",
      "profileImage": "string",
      "remarks": "string",
      "salutationForm": {},
      "salutationId": 1,
      "skypeName": "Ava Chen",
      "streetName": "Ava Chen",
      "titleId": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `addressAddition` | object |  |
| `birthday` | date |  |
| `city` | string |  |
| `contactBranchIds` | object |  |
| `contactGroupIds` | string |  |
| `contactTypeId` | number |  |
| `countryId` | number |  |
| `fax` | string |  |
| `houseNumber` | string |  |
| `id` | number |  |
| `isLead` | boolean |  |
| `languageId` | object |  |
| `mail` | object |  |
| `mailSecond` | object |  |
| `name1` | string |  |
| `name2` | string |  |
| `nr` | string |  |
| `ownerId` | number |  |
| `phoneFixed` | object |  |
| `phoneFixedSecond` | object |  |
| `phoneMobile` | string |  |
| `postcode` | string |  |
| `profileImage` | string |  |
| `remarks` | string |  |
| `salutationForm` | object |  |
| `salutationId` | number |  |
| `skypeName` | string |  |
| `streetName` | string |  |
| `titleId` | object |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Bexio API, this operation is `GET /2.0/contact/:contact_id` (base URL `https://api.bexio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

