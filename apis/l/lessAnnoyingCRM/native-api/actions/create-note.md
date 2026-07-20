# Create Note with Less Annoying CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api.lessannoyingcrm.com/v2`
- **Official documentation:** [Create Note](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Notes#Goto-CreateNote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ContactId` | body | `string` | yes | The contact or company Id to attach the note to. |
| `Note` | body | `string` | yes | Plain-text note body. |
| `DateDisplayedInHistory` | body | `date` | no | Timestamp to use in the contact history view. |
