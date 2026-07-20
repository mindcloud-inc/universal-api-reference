# Get Person with Cloze

Retrieves a person from Cloze.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/people/get`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Get Person](https://api.cloze.com/api-docs/#/paths/v1-people-get/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | query | `boolean` | no | Retrieve the team relation instead of the local relation. |
| `uniqueid` | query | `string` | yes | Person unique identifier such as email address, mobile phone number, or social identifier. |
