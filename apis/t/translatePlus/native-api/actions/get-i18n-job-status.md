# Get I18n Job Status with TranslatePlus

Retrieves i18n translation job status from TranslatePlus.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/translate/i18n/jobs/{job_id}/status`
- **Base URL:** `https://api.translateplus.io`
- **Official documentation:** [Get I18n Job Status](https://docs.translateplus.io/reference/v2/i18n/i18n-job-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | The i18n translation job UUID. |
