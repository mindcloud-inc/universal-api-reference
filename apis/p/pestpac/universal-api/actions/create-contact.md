# PestPac: Create Contact



```
POST https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PestPac `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lastName": "Chen",
  "firstName": "Ava",
  "locationId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lastName": "Chen",
    "firstName": "Ava",
    "locationId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `enteredDate` | date | no |  |
| `lastName` | string | yes |  |
| `firstName` | string | yes |  |
| `address` | string | no |  |
| `address2` | string | no |  |
| `city` | string | no |  |
| `state` | string | no |  |
| `zip` | string | no |  |
| `phone` | string | no |  |
| `fax` | string | no |  |
| `mobilePhone` | string | no |  |
| `email` | string | no |  |
| `comment` | string | no |  |
| `locationId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Address": "string",
      "Address2": "string",
      "AlternatePhone": "string",
      "AlternatePhoneExtension": "string",
      "AnniversaryDate": "string",
      "BirthDate": "string",
      "City": "string",
      "Comment": "string",
      "Company": "string",
      "ContactID": 1,
      "ContactType": "string",
      "EMail": "ava@example.com",
      "Fax": "string",
      "FaxExtension": "string",
      "FirstName": "Ava",
      "HomeAddress": "string",
      "HomeAddress2": "string",
      "HomeCity": "string",
      "HomePhone": "string",
      "HomePhoneExtension": "string",
      "HomeState": "string",
      "HomeZip": "string",
      "JobTitle": "string",
      "LastName": "Chen",
      "MobilePhone": "string",
      "MobilePhoneExtension": "string",
      "NameofAssistant": "Ava Chen",
      "NameofSpouse": "Ava Chen",
      "Nickname": "Ava Chen",
      "Phone": "string",
      "PhoneExtension": "string",
      "PronunciationOfName": "Ava Chen",
      "State": "string",
      "Title": "string",
      "UserDefinedFields": [
        "string"
      ],
      "Zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Address` | string |  |
| `Address2` | string |  |
| `AlternatePhone` | string |  |
| `AlternatePhoneExtension` | string |  |
| `AnniversaryDate` | string |  |
| `BirthDate` | string |  |
| `City` | string |  |
| `Comment` | string |  |
| `Company` | string |  |
| `ContactID` | number |  |
| `ContactType` | string |  |
| `EMail` | string |  |
| `Fax` | string |  |
| `FaxExtension` | string |  |
| `FirstName` | string |  |
| `HomeAddress` | string |  |
| `HomeAddress2` | string |  |
| `HomeCity` | string |  |
| `HomePhone` | string |  |
| `HomePhoneExtension` | string |  |
| `HomeState` | string |  |
| `HomeZip` | string |  |
| `JobTitle` | string |  |
| `LastName` | string |  |
| `MobilePhone` | string |  |
| `MobilePhoneExtension` | string |  |
| `NameofAssistant` | string |  |
| `NameofSpouse` | string |  |
| `Nickname` | string |  |
| `Phone` | string |  |
| `PhoneExtension` | string |  |
| `PronunciationOfName` | string |  |
| `State` | string |  |
| `Title` | string |  |
| `UserDefinedFields` | array<string> |  |
| `Zip` | string |  |

## Native endpoint

Through the native PestPac API, this operation is `POST Contacts` (base URL `https://api.workwave.com/pestpac/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

