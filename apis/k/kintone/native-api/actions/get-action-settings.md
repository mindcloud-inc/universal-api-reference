# Get Action Settings with Kintone

Retrieves action settings from Kintone.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/actions.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [Get Action Settings](https://kintone.dev/en/docs/kintone/rest-api/apps/settings/get-actions/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app` | query | `number` | yes | The Kintone app ID. |
| `lang` | query | `string` | no | Optional language code used for localized settings. |
