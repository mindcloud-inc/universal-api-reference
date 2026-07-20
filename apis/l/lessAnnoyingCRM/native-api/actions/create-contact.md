# Create Contact with Less Annoying CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api.lessannoyingcrm.com/v2`
- **Official documentation:** [Create Contact](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Contacts#Goto-CreateContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `IsCompany` | body | `boolean` | yes | Whether to create a company record instead of a contact record. |
| `AssignedTo` | body | `string` | yes | User Id that should own the new record. |
| `Name` | body | `string` | yes | Full name of the contact or company. |
| `Company Name` | body | `string` | no | Company name for the record when applicable. |
| `Job Title` | body | `string` | no | Job title for the contact. |
| `Background Info` | body | `string` | no | Additional background information. |
| `Birthday` | body | `date` | no | Birthday for the contact. |
