# Create Encounter with Cerbo

Creates a new encounter in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/encounters`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Create Encounter](https://docs.cer.bo/#tag/Encounters/operation/createEncounter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pt_id` | body | `number` | no | A valid ID of a non-archived patient. |
| `date_of_service` | body | `date` | no | A time stamp (YYYY-MM-DD format preferred) representing the date the encounter took or will take place. Can be future or past. |
| `title` | body | `string` | no | The title of the encounter note. |
| `content` | body | `string` | no | The plaintext-formatted text of the encounter note. |
| `encounter_type` | body | `string` | no | The two-letter abbreviation of the type of encounter note you are creating. |
| `owner` | body | `number` | no | A valid ID of a non-archived, non-resource user who is the expected owner/manager of the note. Default is the API “user” itself. |
| `parent_encounter` | body | `number` | no | The valid ID of an existing encounter for the designated patient. If set, the new note will be filed as a sub-note of the designated parent encounter. The parent note must belong to the patient set by pt_id and it must not be a sub-note itself. |
