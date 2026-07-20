# Create Lead with Insightly

Creates a new lead in Insightly.

## Endpoint

- **Method:** `POST`
- **Path:** `{apiBaseUrl}Leads`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [Create Lead](https://api.insightly.com/v3.1/Help#!/Leads/AddEntity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FIRST_NAME` | body | `string` | no | The lead's first name. |
| `LAST_NAME` | body | `string` | yes | The lead's last name. |
| `LEAD_SOURCE_ID` | body | `number` | yes | The Lead Source ID. |
| `LEAD_STATUS_ID` | body | `number` | yes | The Lead Status ID. |
| `EMAIL` | body | `string` | no | The lead's email address. |
| `PHONE` | body | `string` | no | The lead's phone number. |
| `TITLE` | body | `string` | no | The lead's job title. |
