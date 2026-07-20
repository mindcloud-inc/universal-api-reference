# Get Form Fields with Kintone

Retrieves app form fields from Kintone.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/form/fields.json`
- **Base URL:** `{baseUrl}/k/v1`
- **Official documentation:** [Get Form Fields](https://kintone.dev/en/docs/kintone/rest-api/apps/form/get-form-fields/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app` | query | `number` | yes | The Kintone app ID. |
| `lang` | query | `string` | no | Optional language code used for localized settings. |
