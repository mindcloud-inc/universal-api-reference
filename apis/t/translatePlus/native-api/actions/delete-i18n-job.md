# Delete I18n Job with TranslatePlus

Deletes an existing i18n translation job from TranslatePlus.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/translate/i18n/jobs/{job_id}`
- **Base URL:** `https://api.translateplus.io`
- **Official documentation:** [Delete I18n Job](https://docs.translateplus.io/reference/v2/i18n/i18n-delete-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | The i18n translation job UUID. |
