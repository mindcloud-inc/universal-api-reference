# Update Custom Field with Moosend

Updates an existing custom field in Moosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/{{MailingListID}}/customfields/{{CustomFieldID}}/update.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Update Custom Field](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54563-Update-a-custom-field?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list containing the custom field. |
| `CustomFieldID` | path | `string` | yes | The ID of the custom field to be updated. |
| `Name` | body | `string` | yes | The name of the custom field. |
| `CustomFieldType` | body | `string` | no | Specifies the data type of the custom field. This must be one of the following values. Text (Default) - accepts any text value as input. Number - accepts only numeric values as input. DateTime - accepts only date values as input, with or without time. SingleSelectDropdown - accepts only values explicitly defined in a list. CheckBox - accepts only values of true or false. |
| `Options` | body | `string` | no | If you want to update a SingleSelectDropdown custom field, you must set this parameter to specify the available options for the user to choose from. Use a comma (,) to separate different options. |
| `IsRequired` | body | `boolean` | no | Specifies whether the custom field is mandatory or not when adding a subscriber to your list. You must specify a value of true or false (Default). |
| `IsHidden` | body | `boolean` | no | Specifies whether the custom field is visible to your subscribers in the Update Profile page. You must specify a value of true or false (Default). |
