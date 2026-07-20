# Get Company with Cloze

Retrieves a company from Cloze.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/companies/get`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Get Company](https://api.cloze.com/api-docs/#/paths/v1-companies-get/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | query | `boolean` | no | Retrieve the team relation instead of the local relation. |
| `uniqueid` | query | `string` | yes | Company unique identifier such as domain name, email address, phone number, or social identifier. |
