# UKG Pro: Get Employee Changes



```
GET https://connect.mindcloud.co/v1/universal/ukgPro/latest/actions/get-employee-changes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UKG Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ukgPro/latest/actions/get-employee-changes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ukgPro/latest/actions/get-employee-changes?${params}`, {
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
| `employeeId` | string | no |  |
| `endDate` | string | no |  |
| `startDate` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalName1": "Ava Chen",
      "additionalName2": "Ava Chen",
      "addressCity": "Ava Chen",
      "addressCountry": "string",
      "addressCounty": "string",
      "addressId": "string",
      "addressIsOnTaxBoundary": true,
      "addressLatitude": 1,
      "addressLine1": "string",
      "addressLine2": "string",
      "addressLine3": "string",
      "addressLine4": "string",
      "addressSms": "string",
      "addressState": "string",
      "addressZipCode": "string",
      "cellPhoneNumber": "string",
      "companyId": "string",
      "dateOfBirth": "2026-05-07T12:00:00.000Z",
      "disabilityType": "string",
      "emailAddress": "ava@example.com",
      "emailAddressAlternate": "ava@example.com",
      "employeeId": "string",
      "ethnicDescription": "string",
      "ethnicIdCode": "string",
      "firstName": "Ava",
      "formerName": "Ava Chen",
      "gender": "string",
      "healthBloodType": "string",
      "healthEyes": "string",
      "healthHair": "string",
      "healthHeightFeet": 1,
      "healthHeightInches": 1,
      "healthLastDonateDate": "2026-05-07T12:00:00.000Z",
      "healthWeight": 1,
      "homePhone": "string",
      "homePhoneCountry": "string",
      "homePhoneID": "string",
      "homePhoneIsPrivate": true,
      "integrationRecordId": "string",
      "isDisabled": true,
      "isSmoker": true,
      "lastName": "Chen",
      "lastNameNotSameAsSSCard": true,
      "maritalStatusCode": "string",
      "middleName": "Ava Chen",
      "namePrefixCode": "Ava Chen",
      "nameSuffixCode": "Ava Chen",
      "nationality1": "string",
      "nationality2": "string",
      "nationality3": "string",
      "originCountry": "string",
      "originLocation": "string",
      "personId": "string",
      "preferredName": "Ava Chen",
      "previousSSN": "string",
      "ssn": "string",
      "ssnIsSuppressed": true,
      "userID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalName1` | string |  |
| `additionalName2` | string |  |
| `addressCity` | string |  |
| `addressCountry` | string |  |
| `addressCounty` | string |  |
| `addressId` | string |  |
| `addressIsOnTaxBoundary` | boolean |  |
| `addressLatitude` | number |  |
| `addressLine1` | string |  |
| `addressLine2` | string |  |
| `addressLine3` | string |  |
| `addressLine4` | string |  |
| `addressSms` | string |  |
| `addressState` | string |  |
| `addressZipCode` | string |  |
| `cellPhoneNumber` | string |  |
| `companyId` | string |  |
| `dateOfBirth` | date |  |
| `disabilityType` | string |  |
| `emailAddress` | string |  |
| `emailAddressAlternate` | string |  |
| `employeeId` | string |  |
| `ethnicDescription` | string |  |
| `ethnicIdCode` | string |  |
| `firstName` | string |  |
| `formerName` | string |  |
| `gender` | string |  |
| `healthBloodType` | string |  |
| `healthEyes` | string |  |
| `healthHair` | string |  |
| `healthHeightFeet` | number |  |
| `healthHeightInches` | number |  |
| `healthLastDonateDate` | date |  |
| `healthWeight` | number |  |
| `homePhone` | string |  |
| `homePhoneCountry` | string |  |
| `homePhoneID` | string |  |
| `homePhoneIsPrivate` | boolean |  |
| `integrationRecordId` | string |  |
| `isDisabled` | boolean |  |
| `isSmoker` | boolean |  |
| `lastName` | string |  |
| `lastNameNotSameAsSSCard` | boolean |  |
| `maritalStatusCode` | string |  |
| `middleName` | string |  |
| `namePrefixCode` | string |  |
| `nameSuffixCode` | string |  |
| `nationality1` | string |  |
| `nationality2` | string |  |
| `nationality3` | string |  |
| `originCountry` | string |  |
| `originLocation` | string |  |
| `personId` | string |  |
| `preferredName` | string |  |
| `previousSSN` | string |  |
| `ssn` | string |  |
| `ssnIsSuppressed` | boolean |  |
| `userID` | string |  |

## Native endpoint

Through the native UKG Pro API, this operation is `GET personnel/v1/employee-changes/:employeeId` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee-changes.md) for the provider-specific parameters and requirements.

