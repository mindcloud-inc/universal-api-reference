# Export Form Answers with Florm

Creates an export task for Florm form answers.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/export/form/answers`
- **Base URL:** `https://api.florm.io`
- **Official documentation:** [Export Form Answers](https://api.florm.io/docs#/default/export_answers_form_v1_export_form_answers_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Export file type. |
| `form_guid` | body | `string` | yes | GUID of the Florm form to export answers for. |
