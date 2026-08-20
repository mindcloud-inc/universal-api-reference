# Aspire: Update Contact

Update an existing contact record.

```
PUT https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact.contactId": 1,
  "contact.firstName": "Ava",
  "contact.lastName": "Chen",
  "contact.contactTypeId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact.contactId": 1,
    "contact.firstName": "Ava",
    "contact.lastName": "Chen",
    "contact.contactTypeId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact` | object | no |  |
| `contact.contactId` | list<number> | yes |  |
| `homeAddress.addressLine1` | string | no |  |
| `officeAddress.addressLine1` | string | no |  |
| `contact.firstName` | string | yes |  |
| `homeAddress` | object | no |  |
| `homeAddress.addressLine2` | string | no |  |
| `officeAddress.addressLine2` | string | no |  |
| `contact.lastName` | string | yes |  |
| `homeAddress.city` | string | no |  |
| `officeAddress` | object | no |  |
| `officeAddress.city` | string | no |  |
| `contact.companyId` | list<number> | no |  |
| `contactTags` | string<string> | no | Accepts multiple values as an array. |
| `homeAddress.stateProvinceCode` | string | no |  |
| `officeAddress.stateProvinceCode` | string | no |  |
| `contact.contactTypeId` | list<number> | yes | Unique identifier for the contact type (integer(int32)) |
| `homeAddress.zipCode` | string | no |  |
| `officeAddress.zipCode` | string | no |  |
| `payScheduleId` | list<number> | no |  |
| `contact.branchId` | list<number> | no |  |
| `updateOpportunities` | boolean | no |  |
| `contact.ownerContactId` | list<number> | no |  |
| `resendEmails` | boolean | no |  |
| `contact.ownerContactName` | string | no |  |
| `UpdateTags` | boolean | no |  |
| `contact.salutation` | string | no |  |
| `contact.prospectRating` | list<number> | no |  |
| `contact.prospectRatingName` | string | no |  |
| `contact.title` | string | no |  |
| `contact.email` | string | no |  |
| `contact.mobilePhone` | string | no |  |
| `contact.officePhone` | string | no |  |
| `contact.homePhone` | string | no |  |
| `contact.Fax` | string | no |  |
| `contact.Notes` | string | no |  |
| `contact.createdByUserName` | string | no |  |
| `contact.employeeNumber` | string | no |  |
| `contact.website` | string | no |  |
| `contact.employeePin` | string | no |  |
| `contact.accountingSyncId` | string | no |  |
| `contact.externalContactReference` | string | no |  |
| `contact.terminationDate` | string | no | Example: "2024-11-21T04:11:18.514Z" |
| `contact.hRNotes` | string | no |  |
| `contact.defaultWorkersCompId` | list<number> | no |  |
| `contact.defaultWorkCompStateProvince` | string | no | The full State/Province Name (i.e. "Illinois", "Oregon") |
| `contact.defaultWorkersCompStateProvinceCode` | string | no | The State/Province code in ISO3 standard format. (i.e "IL" or "OR") |
| `contact.active` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": 1,
      "email": "ava@example.com",
      "employeeNumber": "string",
      "externalContactReference": "string",
      "firstName": "Ava",
      "lastName": "Chen",
      "mobile": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | number |  |
| `email` | string |  |
| `employeeNumber` | string |  |
| `externalContactReference` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `mobile` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Aspire API, this operation is `PUT Contacts` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

