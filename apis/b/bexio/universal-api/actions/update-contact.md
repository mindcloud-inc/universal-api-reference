# Bexio: Update Contact

Updates a contact in Bexio.

```
PUT https://connect.mindcloud.co/v1/universal/bexio/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bexio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bexio/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "1",
  "contactTypeId": "1",
  "name1": "Example Company",
  "userId": "1",
  "ownerId": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bexio/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "1",
    "contactTypeId": "1",
    "name1": "Example Company",
    "userId": "1",
    "ownerId": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | yes | The id of the contact. Example: `1`. |
| `contactTypeId` | number | yes | Use 1 for companies or 2 for persons. Example: `1`. |
| `name1` | string | yes | Company name when contact type is company, otherwise last name. Example: `Example Company`. |
| `name2` | string | no | Company addition when contact type is company, otherwise first name. Example: `Operations`. |
| `mail` | string | no | Primary email address. Example: `contact@example.org`. |
| `phoneMobile` | string | no | Mobile phone number. Example: `+41 79 123 45 67`. |
| `streetName` | string | no | Required if house number or address addition is provided. Example: `Smith Street`. |
| `houseNumber` | string | no | Requires street name when provided. Example: `77`. |
| `postcode` | string | no | Postal code. Example: `8004`. |
| `city` | string | no | City. Example: `Zurich`. |
| `countryId` | number | no | References a country object. Example: `1`. |
| `userId` | number | yes | References a user object. Example: `1`. |
| `ownerId` | number | yes | Owner id. Example: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addressAddition` | string | no | Requires street name when provided. Example: `Building C`. |
| `nr` | string | no | If set to null, the number will be assigned automatically. Must be a number, can also be used as integer. Example: `10001`. |
| `salutationId` | number | no | References a salutation object. Example: `2`. |
| `salutationForm` | number | no | Salutation form value. |
| `titleId` | number | no | References a title object. |
| `birthday` | date | no | Birthday date. Example: `1990-01-31`. |
| `mailSecond` | string | no | Secondary email address. Example: `billing@example.org`. |
| `phoneFixed` | string | no | Primary fixed phone number. Example: `+41 44 123 45 67`. |
| `phoneFixedSecond` | string | no | Secondary fixed phone number. Example: `+41 44 987 65 43`. |
| `fax` | string | no | Fax number. Example: `+41 44 123 45 68`. |
| `url` | string | no | Website URL. Example: `https://example.org`. |
| `skypeName` | string | no | Skype name. Example: `example.company`. |
| `remarks` | string | no | Remarks. Example: `Important customer`. |
| `languageId` | number | no | References a language object. Example: `1`. |
| `contactGroupIds` | string | no | References one or more contact group objects. Accepts multiple values in one string, delimited by `,`. Example: `1,2`. |
| `contactBranchIds` | string | no | References one or more contact sector objects. Accepts multiple values in one string, delimited by `,`. Example: `3,4`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "addressAddition": {},
      "birthday": "2026-05-07T12:00:00.000Z",
      "city": "string",
      "contactBranchIds": {},
      "contactGroupIds": {},
      "contactTypeId": 1,
      "countryId": {},
      "fax": "string",
      "houseNumber": {},
      "id": 1,
      "isLead": true,
      "languageId": {},
      "mail": "string",
      "mailSecond": "string",
      "name1": "Ava Chen",
      "name2": "Ava Chen",
      "nr": "string",
      "ownerId": 1,
      "phoneFixed": "string",
      "phoneFixedSecond": "string",
      "phoneMobile": "string",
      "postcode": "string",
      "profileImage": "string",
      "remarks": "string",
      "salutationForm": {},
      "salutationId": 1,
      "skypeName": "Ava Chen",
      "streetName": {},
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
| `address` | object |  |
| `addressAddition` | object |  |
| `birthday` | date |  |
| `city` | string |  |
| `contactBranchIds` | object |  |
| `contactGroupIds` | object |  |
| `contactTypeId` | number |  |
| `countryId` | object |  |
| `fax` | string |  |
| `houseNumber` | object |  |
| `id` | number |  |
| `isLead` | boolean |  |
| `languageId` | object |  |
| `mail` | string |  |
| `mailSecond` | string |  |
| `name1` | string |  |
| `name2` | string |  |
| `nr` | string |  |
| `ownerId` | number |  |
| `phoneFixed` | string |  |
| `phoneFixedSecond` | string |  |
| `phoneMobile` | string |  |
| `postcode` | string |  |
| `profileImage` | string |  |
| `remarks` | string |  |
| `salutationForm` | object |  |
| `salutationId` | number |  |
| `skypeName` | string |  |
| `streetName` | object |  |
| `titleId` | object |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Bexio API, this operation is `POST /2.0/contact/:contact_id` (base URL `https://api.bexio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

