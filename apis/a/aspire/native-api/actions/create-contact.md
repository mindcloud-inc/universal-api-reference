# Create Contact with Aspire

Add a new contact.

## Endpoint

- **Method:** `POST`
- **Path:** `Contacts`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Contact](https://guide.youraspire.com/apidocs/contacts-6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Contact` | body | `object` | no | — |
| `Contact.Active` | body | `boolean` | yes | — |
| `HomeAddress.AddressLine1` | body | `string` | no | — |
| `OfficeAddress.AddressLine1` | body | `string` | no | — |
| `Contact.FirstName` | body | `string` | yes | — |
| `HomeAddress.AddressLine2` | body | `string` | no | — |
| `officeAddress` | body | `object` | no | — |
| `OfficeAddress.AddressLine2` | body | `string` | no | — |
| `Contact.LastName` | body | `string` | yes | — |
| `homeAddress` | body | `object` | no | — |
| `HomeAddress.City` | body | `string` | no | — |
| `OfficeAddress.City` | body | `string` | no | — |
| `Contact.CompanyID` | body | `list` | no | — |
| `ContactTags[]` | body | `array<string>` | no | Choose a tag from the dropdown list or enter the TagID (s)  you'd like to add to this Contact. |
| `HomeAddress.StateProvinceCode` | body | `string` | no | Enter a US state, US territory, or Canadian province. Use the two-letter UPS code (e.g., "IL" for Illinois, "ON" for Ontario) or enter the full name and we'll convert it to the two-letter code based on the input. Reference this list for available options: https://www.ups.com/worldshiphelp/WSA/ENU/AppHelp/mergedProjects/CORE/Codes/State_Province_Codes.htm |
| `OfficeAddress.StateProvinceCode` | body | `string` | no | Enter a US state, US territory, or Canadian province. Use the two-letter UPS code (e.g., "IL" for Illinois, "ON" for Ontario) or enter the full name and we'll convert it to the two-letter code based on the input. Reference this list for available options: https://www.ups.com/worldshiphelp/WSA/ENU/AppHelp/mergedProjects/CORE/Codes/State_Province_Codes.htm |
| `Contact.ContactTypeID` | body | `list<number>` | yes | Select an option from the list or enter the unique ID for the contact type (integer(int32)). Example: 3 |
| `HomeAddress.ZipCode` | body | `string` | no | — |
| `OfficeAddress.ZipCode` | body | `string` | no | — |
| `PayScheduleID` | body | `list<number>` | no | — |
| `Contact.BranchID` | body | `list<number>` | no | — |
| `Contact.OwnerContactID` | body | `list<number>` | no | — |
| `Contact.OwnerContactName` | body | `string` | no | — |
| `Contact.Salutation` | body | `string` | no | — |
| `Contact.ProspectRating` | body | `list<number>` | no | — |
| `Contact.Title` | body | `string` | no | — |
| `Contact.Email` | body | `string` | no | — |
| `Contact.MobilePhone` | body | `string` | no | — |
| `Contact.OfficePhone` | body | `string` | no | — |
| `Contact.HomePhone` | body | `string` | no | — |
| `Contact.Fax` | body | `string` | no | — |
| `Contact.Website` | body | `string` | no | — |
| `Contact.Notes` | body | `string` | no | — |
| `Contact.EmployeeNumber` | body | `string` | no | — |
| `Contact.EmployeePin` | body | `string` | no | — |
| `Contact.AccountingSyncID` | body | `string` | no | — |
| `Contact.ExternalContactReference` | body | `string` | no | — |
| `Contact.TerminationDate` | body | `string` | no | Example: "2024-11-21T04:11:18.514Z" |
| `Contact.HRNotes` | body | `string` | no | — |
| `Contact.DefaultWorkersCompID` | body | `string` | no | — |
