# PestPac: Create Location



```
POST https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/create-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PestPac `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/create-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lastName": "Chen",
  "firstName": "Ava",
  "address": "string",
  "city": "string",
  "state": "string",
  "zip": "string",
  "phone": "string",
  "email": "ava@example.com",
  "taxCode": "string",
  "branch": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pestpac/latest/actions/create-location', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lastName": "Chen",
    "firstName": "Ava",
    "address": "string",
    "city": "string",
    "state": "string",
    "zip": "string",
    "phone": "string",
    "email": "ava@example.com",
    "taxCode": "string",
    "branch": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lastName` | string | yes |  |
| `firstName` | string | yes |  |
| `address` | string | yes |  |
| `address2` | string | no |  |
| `city` | string | yes |  |
| `state` | string | yes |  |
| `zip` | string | yes |  |
| `country` | string | no |  |
| `phone` | string | yes |  |
| `mobilePhone` | string | no |  |
| `email` | string | yes |  |
| `website` | string | no |  |
| `active` | boolean | no |  |
| `county` | string | no |  |
| `taxCode` | string | yes |  |
| `comment` | string | no |  |
| `enteredDate` | date | no |  |
| `branch` | string | yes |  |
| `type` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AccountType": "string",
      "Active": true,
      "Address": "string",
      "Address2": "string",
      "AlternatePhone": "string",
      "AlternatePhoneExtension": "string",
      "AutomatedEmails": {},
      "BillToID": 1,
      "Branch": "string",
      "BranchID": 1,
      "Builder": "string",
      "City": "string",
      "Comment": "string",
      "Company": "string",
      "ContactCode": "string",
      "ContactDate": "string",
      "Country": "string",
      "County": "string",
      "Division": "string",
      "DoNotGeocode": true,
      "EMail": "ava@example.com",
      "EnteredDate": "2026-05-07T12:00:00.000Z",
      "Fax": "string",
      "FaxExtension": "string",
      "FirstName": "Ava",
      "GLCode": "string",
      "IncludeInMailings": true,
      "Instructions": "string",
      "InternalIdentifier": "string",
      "LastName": "Chen",
      "Latitude": 1,
      "LocationCode": "string",
      "LocationID": 1,
      "Longitude": 1,
      "MapCode": "string",
      "MobilePhone": "string",
      "MobilePhoneExtension": "string",
      "Phone": "string",
      "PhoneExtension": "string",
      "Prospect": true,
      "PurchaseOrderExpirationDate": "string",
      "PurchaseOrderNumber": "string",
      "RooftopLatitude": 1,
      "RooftopLongitude": 1,
      "Salutation": "string",
      "SalutationName": "Ava Chen",
      "ShowOnLogBook": true,
      "SmsMarketing": true,
      "Source": "string",
      "State": "string",
      "Street": "string",
      "Subdivision": "string",
      "TaxCode": "string",
      "TaxExemptNumber": "string",
      "TaxRate": 1,
      "Title": "string",
      "Type": "string",
      "UserDefinedFields": [
        {}
      ],
      "Website": "string",
      "Zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AccountType` | string |  |
| `Active` | boolean |  |
| `Address` | string |  |
| `Address2` | string |  |
| `AlternatePhone` | string |  |
| `AlternatePhoneExtension` | string |  |
| `AutomatedEmails` | object |  |
| `BillToID` | number |  |
| `Branch` | string |  |
| `BranchID` | number |  |
| `Builder` | string |  |
| `City` | string |  |
| `Comment` | string |  |
| `Company` | string |  |
| `ContactCode` | string |  |
| `ContactDate` | string |  |
| `Country` | string |  |
| `County` | string |  |
| `Division` | string |  |
| `DoNotGeocode` | boolean |  |
| `EMail` | string |  |
| `EnteredDate` | date |  |
| `Fax` | string |  |
| `FaxExtension` | string |  |
| `FirstName` | string |  |
| `GLCode` | string |  |
| `IncludeInMailings` | boolean |  |
| `Instructions` | string |  |
| `InternalIdentifier` | string |  |
| `LastName` | string |  |
| `Latitude` | number |  |
| `LocationCode` | string |  |
| `LocationID` | number |  |
| `Longitude` | number |  |
| `MapCode` | string |  |
| `MobilePhone` | string |  |
| `MobilePhoneExtension` | string |  |
| `Phone` | string |  |
| `PhoneExtension` | string |  |
| `Prospect` | boolean |  |
| `PurchaseOrderExpirationDate` | string |  |
| `PurchaseOrderNumber` | string |  |
| `RooftopLatitude` | number |  |
| `RooftopLongitude` | number |  |
| `Salutation` | string |  |
| `SalutationName` | string |  |
| `ShowOnLogBook` | boolean |  |
| `SmsMarketing` | boolean |  |
| `Source` | string |  |
| `State` | string |  |
| `Street` | string |  |
| `Subdivision` | string |  |
| `TaxCode` | string |  |
| `TaxExemptNumber` | string |  |
| `TaxRate` | number |  |
| `Title` | string |  |
| `Type` | string |  |
| `UserDefinedFields` | array<object> |  |
| `Website` | string |  |
| `Zip` | string |  |

## Native endpoint

Through the native PestPac API, this operation is `POST Locations` (base URL `https://api.workwave.com/pestpac/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-location.md) for the provider-specific parameters and requirements.

