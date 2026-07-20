# Get Views with Kintone

Retrieves app views from Kintone.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/views.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [Get Views](https://kintone.dev/en/docs/kintone/rest-api/apps/view/get-views/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app` | query | `number` | yes | The Kintone app ID. |
| `lang` | query | `string` | no | Optional language code used for localized settings. |
