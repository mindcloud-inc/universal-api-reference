# Update Organisation with Insightly

Updates an existing organisation in Insightly.

## Endpoint

- **Method:** `PUT`
- **Path:** `{apiBaseUrl}Organisations`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [Update Organisation](https://api.insightly.com/v3.1/Help#!/Organisations/UpdateEntity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ORGANISATION_ID` | body | `number` | yes | The Organisation ID to update. |
| `ORGANISATION_NAME` | body | `string` | yes | The organisation name. |
| `PHONE` | body | `string` | no | The organisation phone number. |
| `WEBSITE` | body | `string` | no | The organisation website URL. |
| `BACKGROUND` | body | `string` | no | Background notes for the organisation. |
