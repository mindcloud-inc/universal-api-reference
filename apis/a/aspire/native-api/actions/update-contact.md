# Update Contact with Aspire

Update an existing contact record.

## Endpoint

- **Method:** `PUT`
- **Path:** `Contacts`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update Contact](https://guide.youraspire.com/apidocs/contacts-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Contact` | body | `object` | no | — |
| `Contact.ContactID` | body | `list<number>` | yes | — |
| `HomeAddress.AddressLine1` | body | `string` | no | — |
| `OfficeAddress.AddressLine1` | body | `string` | no | — |
| `Contact.FirstName` | body | `string` | yes | — |
| `HomeAddress` | body | `object` | no | — |
| `HomeAddress.AddressLine2` | body | `string` | no | — |
| `OfficeAddress.AddressLine2` | body | `string` | no | — |
| `Contact.LastName` | body | `string` | yes | — |
| `HomeAddress.City` | body | `string` | no | — |
| `OfficeAddress` | body | `object` | no | — |
| `OfficeAddress.City` | body | `string` | no | — |
| `Contact.CompanyID` | body | `list<number>` | no | — |
| `ContactTags` | body | `string<string>` | no | Send multiple values as a array. |
| `HomeAddress.StateProvinceCode` | body | `string` | no | — |
| `OfficeAddress.StateProvinceCode` | body | `string` | no | — |
| `Contact.ContactTypeID` | body | `list<number>` | yes | Unique identifier for the contact type (integer(int32)) |
| `HomeAddress.ZipCode` | body | `string` | no | — |
| `OfficeAddress.ZipCode` | body | `string` | no | — |
| `PayScheduleID` | body | `list<number>` | no | — |
| `Contact.BranchID` | body | `list<number>` | no | — |
| `UpdateOpportunities` | body | `boolean` | no | — |
| `Contact.OwnerContactID` | body | `list<number>` | no | — |
| `ResendEmails` | body | `boolean` | no | — |
| `Contact.OwnerContactName` | body | `string` | no | — |
| `UpdateTags` | body | `boolean` | no | — |
| `Contact.Salutation` | body | `string` | no | — |
| `Contact.ProspectRating` | body | `list<number>` | no | — |
| `Contact.ProspectRatingName` | body | `string` | no | — |
| `Contact.Title` | body | `string` | no | — |
| `Contact.Email` | body | `string` | no | — |
| `Contact.MobilePhone` | body | `string` | no | — |
| `Contact.OfficePhone` | body | `string` | no | — |
| `Contact.HomePhone` | body | `string` | no | — |
| `Contact.Fax` | body | `string` | no | — |
| `Contact.Notes` | body | `string` | no | — |
| `Contact.CreatedByUserName` | body | `string` | no | — |
| `Contact.EmployeeNumber` | body | `string` | no | — |
| `Contact.Website` | body | `string` | no | — |
| `Contact.EmployeePin` | body | `string` | no | — |
| `Contact.AccountingSyncID` | body | `string` | no | — |
| `Contact.ExternalContactReference` | body | `string` | no | — |
| `Contact.TerminationDate` | body | `string` | no | Example: "2024-11-21T04:11:18.514Z" |
| `Contact.HRNotes` | body | `string` | no | — |
| `Contact.DefaultWorkersCompID` | body | `list<number>` | no | — |
| `Contact.DefaultWorkersCompStateProvince` | body | `string` | no | The full State/Province Name (i.e. "Illinois", "Oregon") |
| `Contact.DefaultWorkersCompStateProvinceCode` | body | `string` | no | The State/Province code in ISO3 standard format. (i.e "IL" or "OR") |
| `Contact.Active` | body | `boolean` | no | — |
