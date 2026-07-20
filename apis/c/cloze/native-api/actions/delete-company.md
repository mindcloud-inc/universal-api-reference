# Delete Company with Cloze

Deletes a company from Cloze.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/companies/delete`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Delete Company](https://api.cloze.com/api-docs/#/paths/v1-companies-delete/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | query | `boolean` | no | Delete the team relation instead of the local relation. |
| `uniqueid` | query | `string` | yes | Company unique identifier such as domain name, email address, phone number, or social identifier. |
