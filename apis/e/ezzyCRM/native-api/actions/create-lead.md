# Create Lead with EzzyCRM

## Endpoint

- **Method:** `POST`
- **Path:** `/api/savelead`
- **Base URL:** `https://ezzycrm.com`
- **Official documentation:** [Create Lead](https://ezzycrm.com/api/PostApiDocument.aspx#savelead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ContactModel` | body | `object` | no | — |
| `ContactModel.FirstName` | body | `string` | yes | — |
| `ContactModel.LastName` | body | `string` | yes | — |
| `ContactModel.Email` | body | `string` | no | — |
| `ContactModel.Title` | body | `string` | no | — |
| `ContactModel.PhoneType` | body | `string` | no | — |
| `ContactModel.Phone` | body | `string` | no | — |
| `ContactModel.Remark` | body | `string` | no | — |
| `OrganizationModel` | body | `object` | no | — |
| `OrganizationModel.OrganizationName` | body | `string` | yes | — |
| `OrganizationModel.Address1` | body | `string` | no | — |
| `OrganizationModel.Address2` | body | `string` | no | — |
| `OrganizationModel.City` | body | `string` | no | — |
| `OrganizationModel.ZipCode` | body | `string` | no | — |
| `OrganizationModel.StateName` | body | `string` | no | — |
| `OrganizationModel.CountryName` | body | `string` | no | — |
| `OrganizationModel.IndustryName` | body | `string` | no | — |
| `UserId` | body | `number` | yes | — |
| `DealTitle` | body | `string` | yes | — |
| `DealValue` | body | `string` | no | — |
| `DealCurrencyId` | body | `number` | yes | — |
| `NoteModel[]` | body | `array<string>` | no | — |
| `PipelineId` | body | `number` | yes | — |
| `StageCode` | body | `string` | yes | — |
| `ExpectedCloseDate` | body | `string` | no | Expected close date in MM/DD/YYYY format. |
| `CustomField1` | body | `string` | no | — |
| `CustomField2` | body | `string` | no | — |
| `CustomField3` | body | `string` | no | — |
| `CustomField4` | body | `string` | no | — |
| `CustomField5` | body | `string` | no | — |
| `CustomField6` | body | `string` | no | — |
| `CustomField7` | body | `string` | no | — |
| `CustomField8` | body | `string` | no | — |
| `CustomField9` | body | `string` | no | — |
| `CustomField10` | body | `string` | no | — |
