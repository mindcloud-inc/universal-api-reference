# Delete Form with Florm

Deletes an existing form from Florm.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/forms/:form_guid`
- **Base URL:** `https://api.florm.io`
- **Official documentation:** [Delete Form](https://api.florm.io/docs#/default/delete_form_v1_forms__form_guid__delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_guid` | path | `string` | yes | GUID of the Florm form to delete. |
