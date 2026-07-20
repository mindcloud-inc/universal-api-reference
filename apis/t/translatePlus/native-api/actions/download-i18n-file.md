# Download I18n File with TranslatePlus

Downloads a translated i18n file from TranslatePlus.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/translate/i18n/jobs/{job_id}/download`
- **Base URL:** `https://api.translateplus.io`
- **Official documentation:** [Download I18n File](https://docs.translateplus.io/reference/v2/i18n/i18n-download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | The i18n translation job UUID. |
| `language_code` | query | `string` | yes | Target language code to download, such as fr. |
