# Microsoft Dynamics 365: Get Workers



```
GET https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/get-workers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/get-workers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/get-workers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "@odata": {
        "context": "string",
        "etag": "string"
      },
      "AddressBooks": "string",
      "AddressCity": "string",
      "AddressCountryRegionId": "string",
      "AddressCountryRegionISOCode": "string",
      "AddressCounty": "string",
      "AddressDistrictName": "Ava Chen",
      "AddressLocationId": "string",
      "AddressNameDescription": "Ava Chen",
      "AddressPurpose": "string",
      "AddressState": "string",
      "AddressStreet": "string",
      "AddressValidFrom": "string",
      "AddressValidTo": "string",
      "AddressZipCode": "string",
      "AllowRehire": "string",
      "AnniversaryDateTime": "string",
      "BirthDate": "string",
      "CitizenshipCountryRegion": "string",
      "DeceasedDate": "string",
      "DisabledVerificationDate": "string",
      "Education": "string",
      "ElectronicLocationId": "string",
      "EthnicOriginId": "string",
      "ExpatriateRulingValidFrom": "string",
      "ExpatriateRulingValidTo": "string",
      "FatherBirthCountryRegion": "string",
      "FirstName": "Ava",
      "Gender": "string",
      "IdentityEmail": "ava@example.com",
      "IdentityProvider": "string",
      "IsDisabled": "string",
      "IsDisabledVeteran": "string",
      "IsExpatriateRulingApplicable": "string",
      "IsFulltimeStudent": "string",
      "KnownAs": "string",
      "LanguageId": "string",
      "LastName": "Chen",
      "LastNamePrefix": "Chen",
      "MaritalStatus": "string",
      "MiddleName": "Ava Chen",
      "MilitaryServiceEndDate": "string",
      "MilitaryServiceStartDate": "string",
      "MotherBirthCountryRegion": "string",
      "Name": "Ava Chen",
      "NameAlias": "Ava Chen",
      "NameSequenceDisplayAs": "Ava Chen",
      "NationalityCountryRegion": "string",
      "NativeLanguageId": "string",
      "NumberOfDependents": 1,
      "ObjectId": "string",
      "OfficeLocation": "string",
      "OfficeLocationId": "string",
      "OriginalHireDateTime": "string",
      "PartyNumber": "string",
      "PartyType": "string",
      "PersonalSuffix": "string",
      "PersonalTitle": "string",
      "PersonBirthCity": "string",
      "PersonBirthCountryRegion": "string",
      "PersonDetailsValidFrom": "string",
      "PersonDetailsValidTo": "string",
      "PersonnelNumber": "string",
      "PersonUserValidFrom": "string",
      "PersonUserValidTo": "string",
      "PhoneticFirstName": "Ava",
      "PhoneticLastName": "Chen",
      "PhoneticMiddleName": "Ava Chen",
      "PrimaryAddressLocation": 1,
      "PrimaryContactEmail": "ava@example.com",
      "PrimaryContactEmailDescription": "ava@example.com",
      "PrimaryContactEmailIsIM": "ava@example.com",
      "PrimaryContactEmailIsPrivate": "ava@example.com",
      "PrimaryContactEmailPurpose": "ava@example.com",
      "PrimaryContactFacebook": "string",
      "PrimaryContactFacebookDescription": "string",
      "PrimaryContactFacebookIsPrivate": "string",
      "PrimaryContactFacebookPurpose": "string",
      "PrimaryContactFax": "string",
      "PrimaryContactFaxDescription": "string",
      "PrimaryContactFaxExtension": "string",
      "PrimaryContactFaxIsPrivate": "string",
      "PrimaryContactFaxPurpose": "string",
      "PrimaryContactLinkedIn": "https://example.com",
      "PrimaryContactLinkedInDescription": "https://example.com",
      "PrimaryContactLinkedInIsPrivate": "https://example.com",
      "PrimaryContactLinkedInPurpose": "https://example.com",
      "PrimaryContactPhone": "string",
      "PrimaryContactPhoneDescription": "string",
      "PrimaryContactPhoneExtension": "string",
      "PrimaryContactPhoneIsMobile": "string",
      "PrimaryContactPhoneIsPrivate": "string",
      "PrimaryContactPhonePurpose": "string",
      "PrimaryContactTwitter": "string",
      "PrimaryContactTwitterDescription": "string",
      "PrimaryContactTwitterIsPrivate": "string",
      "PrimaryContactTwitterPurpose": "string",
      "PrimaryContactURL": "https://example.com",
      "PrimaryContactURLDescription": "https://example.com",
      "PrimaryContactURLIsPrivate": "https://example.com",
      "PrimaryContactURLPurpose": "https://example.com",
      "ProfessionalSuffix": "string",
      "ProfessionalTitle": "string",
      "SeniorityDate": "string",
      "SummaryValidFrom": "string",
      "SummaryValidTo": "string",
      "TitleId": "string",
      "User": "string",
      "VeteranStatusId": "string",
      "WorkerStatus": "string",
      "WorkerType": "string",
      "WorksFromHome": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@odata.context` | string |  |
| `@odata.etag` | string |  |
| `AddressBooks` | string |  |
| `AddressCity` | string |  |
| `AddressCountryRegionId` | string |  |
| `AddressCountryRegionISOCode` | string |  |
| `AddressCounty` | string |  |
| `AddressDistrictName` | string |  |
| `AddressLocationId` | string |  |
| `AddressNameDescription` | string |  |
| `AddressPurpose` | string |  |
| `AddressState` | string |  |
| `AddressStreet` | string |  |
| `AddressValidFrom` | string |  |
| `AddressValidTo` | string |  |
| `AddressZipCode` | string |  |
| `AllowRehire` | string |  |
| `AnniversaryDateTime` | string |  |
| `BirthDate` | string |  |
| `CitizenshipCountryRegion` | string |  |
| `DeceasedDate` | string |  |
| `DisabledVerificationDate` | string |  |
| `Education` | string |  |
| `ElectronicLocationId` | string |  |
| `EthnicOriginId` | string |  |
| `ExpatriateRulingValidFrom` | string |  |
| `ExpatriateRulingValidTo` | string |  |
| `FatherBirthCountryRegion` | string |  |
| `FirstName` | string |  |
| `Gender` | string |  |
| `IdentityEmail` | string |  |
| `IdentityProvider` | string |  |
| `IsDisabled` | string |  |
| `IsDisabledVeteran` | string |  |
| `IsExpatriateRulingApplicable` | string |  |
| `IsFulltimeStudent` | string |  |
| `KnownAs` | string |  |
| `LanguageId` | string |  |
| `LastName` | string |  |
| `LastNamePrefix` | string |  |
| `MaritalStatus` | string |  |
| `MiddleName` | string |  |
| `MilitaryServiceEndDate` | string |  |
| `MilitaryServiceStartDate` | string |  |
| `MotherBirthCountryRegion` | string |  |
| `Name` | string |  |
| `NameAlias` | string |  |
| `NameSequenceDisplayAs` | string |  |
| `NationalityCountryRegion` | string |  |
| `NativeLanguageId` | string |  |
| `NumberOfDependents` | number |  |
| `ObjectId` | string |  |
| `OfficeLocation` | string |  |
| `OfficeLocationId` | string |  |
| `OriginalHireDateTime` | string |  |
| `PartyNumber` | string |  |
| `PartyType` | string |  |
| `PersonalSuffix` | string |  |
| `PersonalTitle` | string |  |
| `PersonBirthCity` | string |  |
| `PersonBirthCountryRegion` | string |  |
| `PersonDetailsValidFrom` | string |  |
| `PersonDetailsValidTo` | string |  |
| `PersonnelNumber` | string |  |
| `PersonUserValidFrom` | string |  |
| `PersonUserValidTo` | string |  |
| `PhoneticFirstName` | string |  |
| `PhoneticLastName` | string |  |
| `PhoneticMiddleName` | string |  |
| `PrimaryAddressLocation` | number |  |
| `PrimaryContactEmail` | string |  |
| `PrimaryContactEmailDescription` | string |  |
| `PrimaryContactEmailIsIM` | string |  |
| `PrimaryContactEmailIsPrivate` | string |  |
| `PrimaryContactEmailPurpose` | string |  |
| `PrimaryContactFacebook` | string |  |
| `PrimaryContactFacebookDescription` | string |  |
| `PrimaryContactFacebookIsPrivate` | string |  |
| `PrimaryContactFacebookPurpose` | string |  |
| `PrimaryContactFax` | string |  |
| `PrimaryContactFaxDescription` | string |  |
| `PrimaryContactFaxExtension` | string |  |
| `PrimaryContactFaxIsPrivate` | string |  |
| `PrimaryContactFaxPurpose` | string |  |
| `PrimaryContactLinkedIn` | string |  |
| `PrimaryContactLinkedInDescription` | string |  |
| `PrimaryContactLinkedInIsPrivate` | string |  |
| `PrimaryContactLinkedInPurpose` | string |  |
| `PrimaryContactPhone` | string |  |
| `PrimaryContactPhoneDescription` | string |  |
| `PrimaryContactPhoneExtension` | string |  |
| `PrimaryContactPhoneIsMobile` | string |  |
| `PrimaryContactPhoneIsPrivate` | string |  |
| `PrimaryContactPhonePurpose` | string |  |
| `PrimaryContactTwitter` | string |  |
| `PrimaryContactTwitterDescription` | string |  |
| `PrimaryContactTwitterIsPrivate` | string |  |
| `PrimaryContactTwitterPurpose` | string |  |
| `PrimaryContactURL` | string |  |
| `PrimaryContactURLDescription` | string |  |
| `PrimaryContactURLIsPrivate` | string |  |
| `PrimaryContactURLPurpose` | string |  |
| `ProfessionalSuffix` | string |  |
| `ProfessionalTitle` | string |  |
| `SeniorityDate` | string |  |
| `SummaryValidFrom` | string |  |
| `SummaryValidTo` | string |  |
| `TitleId` | string |  |
| `User` | string |  |
| `VeteranStatusId` | string |  |
| `WorkerStatus` | string |  |
| `WorkerType` | string |  |
| `WorksFromHome` | string |  |

## Native endpoint

Through the native Microsoft Dynamics 365 API, this operation is `GET /Workers` (base URL `{{credentials.baseURL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workers.md) for the provider-specific parameters and requirements.

