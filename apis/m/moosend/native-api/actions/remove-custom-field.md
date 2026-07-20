# Remove Custom Field with Moosend

Deletes an existing custom field from Moosend.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/lists/{{MailingListID}}/customfields/{{CustomFieldID}}/delete.json`
- **Base URL:** `https://api.moosend.com/v3`
- **Official documentation:** [Remove Custom Field](https://docs.moosend.com/api-documentation/articles/KnowledgeBase/54566-Remove-a-custom-field?lang=en_US)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MailingListID` | path | `string` | yes | The ID of the email list containing the custom field. |
| `CustomFieldID` | path | `string` | yes | The ID of the custom field to be deleted. |
