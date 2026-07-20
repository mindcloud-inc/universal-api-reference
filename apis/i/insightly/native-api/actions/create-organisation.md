# Create Organisation with Insightly

Creates a new organisation in Insightly.

## Endpoint

- **Method:** `POST`
- **Path:** `{apiBaseUrl}Organisations`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [Create Organisation](https://api.insightly.com/v3.1/Help#!/Organisations/AddEntity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ORGANISATION_NAME` | body | `string` | yes | The organisation name. |
| `PHONE` | body | `string` | no | The organisation phone number. |
| `WEBSITE` | body | `string` | no | The organisation website URL. |
| `BACKGROUND` | body | `string` | no | Background notes for the organisation. |
