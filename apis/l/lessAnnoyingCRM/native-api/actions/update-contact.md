# Update Contact with Less Annoying CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api.lessannoyingcrm.com/v2`
- **Official documentation:** [Update Contact](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Contacts#Goto-EditContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ContactId` | body | `string` | yes | The contact or company Id to update. |
| `AssignedTo` | body | `string` | no | User Id that should own the record. |
| `Name` | body | `string` | no | Updated full name of the contact or company. |
| `Company Name` | body | `string` | no | Updated company name. |
| `Job Title` | body | `string` | no | Updated job title for the contact. |
| `Background Info` | body | `string` | no | Updated background information. |
| `Birthday` | body | `date` | no | Updated birthday for the contact. |
