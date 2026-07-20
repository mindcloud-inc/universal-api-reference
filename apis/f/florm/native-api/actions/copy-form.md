# Copy Form with Florm

Creates a copy of a Florm form.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/forms/:form_guid/copy`
- **Base URL:** `https://api.florm.io`
- **Official documentation:** [Copy Form](https://api.florm.io/docs#/default/copy_form_v1_forms__form_guid__copy_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_guid` | path | `string` | yes | GUID of the Florm form to copy. |
