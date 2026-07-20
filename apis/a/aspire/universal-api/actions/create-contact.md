# Aspire: Create Contact

Add a new contact.

```
POST https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact.Active": true,
  "contact.FirstName": "Ava",
  "contact.LastName": "Chen",
  "contact.contactTypeId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact.Active": true,
    "contact.FirstName": "Ava",
    "contact.LastName": "Chen",
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
| `contact.Active` | boolean | yes |  |
| `homeAddress.addressLine1` | string | no |  |
| `officeAddress.addressLine1` | string | no |  |
| `contact.FirstName` | string | yes |  |
| `homeAddress.addressLine2` | string | no |  |
| `officeAddress` | object | no |  |
| `officeAddress.addressLine2` | string | no |  |
| `contact.LastName` | string | yes |  |
| `homeAddress` | object | no |  |
| `homeAddress.city` | string | no |  |
| `officeAddress.city` | string | no |  |
| `contact.company` | list | no |  |
| `contactTags[]` | array<string> | no | Choose a tag from the dropdown list or enter the TagID (s) you'd like to add to this Contact. |
| `homeAddress.stateProvinceCode` | string | no | Enter a US state, US territory, or Canadian province. Use the two-letter UPS code (e.g., "IL" for Illinois, "ON" for Ontario) or enter the full name and we'll convert it to the two-letter code based on the input. Reference this list for available options: https://www.ups.com/worldshiphelp/WSA/ENU/AppHelp/mergedProjects/CORE/Codes/State_Province_Codes.htm |
| `officeAddress.stateProvinceCode` | string | no | Enter a US state, US territory, or Canadian province. Use the two-letter UPS code (e.g., "IL" for Illinois, "ON" for Ontario) or enter the full name and we'll convert it to the two-letter code based on the input. Reference this list for available options: https://www.ups.com/worldshiphelp/WSA/ENU/AppHelp/mergedProjects/CORE/Codes/State_Province_Codes.htm |
| `contact.contactTypeId` | list<number> | yes | Select an option from the list or enter the unique ID for the contact type (integer(int32)). Example: 3 |
| `homeAddress.zipCode` | string | no |  |
| `officeAddress.zipCode` | string | no |  |
| `payScheduleId` | list<number> | no |  |
| `contact.branchId` | list<number> | no |  |
| `contact.ownerContactId` | list<number> | no |  |
| `contact.ownerContactName` | string | no |  |
| `contact.salutation` | string | no |  |
| `contact.prospectRating` | list<number> | no |  |
| `contact.title` | string | no |  |
| `contact.email` | string | no |  |
| `contact.mobilePhone` | string | no |  |
| `contact.officePhone` | string | no |  |
| `contact.homePhone` | string | no |  |
| `contact.Fax` | string | no |  |
| `contact.website` | string | no |  |
| `contact.Notes` | string | no |  |
| `contact.employeeNumber` | string | no |  |
| `contact.employeePin` | string | no |  |
| `contact.accountingSyncId` | string | no |  |
| `contact.externalContactReference` | string | no |  |
| `contact.terminationDate` | string | no | Example: "2024-11-21T04:11:18.514Z" |
| `contact.hRNotes` | string | no |  |
| `contact.defaultWorkersCompId` | string | no |  |

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

Through the native Aspire API, this operation is `POST Contacts` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

