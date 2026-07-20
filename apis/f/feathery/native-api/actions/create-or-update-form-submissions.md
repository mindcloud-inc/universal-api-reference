# Create or Update Form Submissions with Feathery

## Endpoint

- **Method:** `POST`
- **Path:** `/api/form/submission/`
- **Base URL:** `https://api.feathery.io`
- **Official documentation:** [Create or Update Form Submissions](https://api-docs.feathery.io/#create-or-update-form-submissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | body | `object` | yes | A mapping from field identifier to value. |
| `user_id` | body | `string` | no | A new or existing user ID. If omitted, Feathery generates one. |
| `forms[]` | body | `array<string>` | no | An array of form IDs to initialize submissions for. |
| `complete` | body | `boolean` | no | Whether the submission should be marked complete. |
| `documents[]` | body | `array<object>` | no | An array of document generation objects, optionally with output locations for spreadsheet cells. |
