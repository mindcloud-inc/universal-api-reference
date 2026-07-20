# Update Note with Less Annoying CRM

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://api.lessannoyingcrm.com/v2`
- **Official documentation:** [Update Note](https://account.lessannoyingcrm.com/api_docs/v2/Core_Functions/Notes#Goto-EditNote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `NoteId` | body | `string` | yes | The note Id to update. |
| `Note` | body | `string` | no | Updated plain-text note body. |
| `DateDisplayedInHistory` | body | `date` | no | Updated history timestamp for the note. |
