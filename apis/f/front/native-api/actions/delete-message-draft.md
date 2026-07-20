# Delete Message Draft with Front

Deletes an existing message draft from Front.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/drafts/:draft_id`
- **Base URL:** `https://api2.frontapp.com`
- **Official documentation:** [Delete Message Draft](https://dev.frontapp.com/reference/delete-draft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `draft_id` | path | `string` | yes | The draft ID. |
| `version` | body | `string` | yes | Version of the draft. |
