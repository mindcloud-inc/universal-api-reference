# Update Lead with Insightly

Updates an existing lead in Insightly.

## Endpoint

- **Method:** `PUT`
- **Path:** `{apiBaseUrl}Leads`
- **Base URL:** `https://api.na1.insightly.com/v3.1/`
- **Official documentation:** [Update Lead](https://api.insightly.com/v3.1/Help#!/Leads/UpdateEntity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `LEAD_ID` | body | `number` | yes | The Lead ID to update. |
| `FIRST_NAME` | body | `string` | no | The lead's first name. |
| `LAST_NAME` | body | `string` | yes | The lead's last name. |
| `LEAD_SOURCE_ID` | body | `number` | yes | The Lead Source ID. |
| `LEAD_STATUS_ID` | body | `number` | yes | The Lead Status ID. |
| `EMAIL` | body | `string` | no | The lead's email address. |
| `PHONE` | body | `string` | no | The lead's phone number. |
| `TITLE` | body | `string` | no | The lead's job title. |
