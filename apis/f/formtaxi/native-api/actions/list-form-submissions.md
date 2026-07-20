# List Form Submissions with Form.taxi

Retrieves form submissions from Form.taxi.

## Endpoint

- **Method:** `GET`
- **Path:** `/form/submissions/:formCode`
- **Base URL:** `https://form.taxi/api/v1`
- **Official documentation:** [List Form Submissions](https://docs.form.taxi/en/api-form-submissions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_code` | path | `string` | yes | The unique code of the form. Form.taxi shows it in the form settings. |
| `since` | query | `string` | no | Return only submissions created on or after this ISO 8601 timestamp. |
| `spam` | query | `boolean` | no | Include submissions from the spam folder when set to true. |
| `attachments` | query | `boolean` | no | Set to false to exclude file attachments from the response. |
