# Get General Settings with Kintone

Retrieves general app settings from Kintone.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/settings.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [Get General Settings](https://kintone.dev/en/docs/kintone/rest-api/apps/settings/get-general-settings/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app` | query | `number` | yes | The Kintone app ID. |
| `lang` | query | `string` | no | Optional language code used for localized settings. |
