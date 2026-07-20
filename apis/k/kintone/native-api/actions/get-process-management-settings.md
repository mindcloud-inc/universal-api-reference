# Get Process Management Settings with Kintone

Retrieves process management settings from Kintone.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/status.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [Get Process Management Settings](https://kintone.dev/en/docs/kintone/rest-api/apps/settings/get-process-management-settings/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app` | query | `number` | yes | The Kintone app ID. |
| `lang` | query | `string` | no | Optional language code used for localized settings. |
