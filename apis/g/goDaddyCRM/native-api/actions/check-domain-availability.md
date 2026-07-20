# Check Domain Availability with GoDaddy CRM

Checks domain availability with the GoDaddy API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/domains/available`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Check Domain Availability](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Domain name whose availability is to be checked. |
| `checkType` | query | `string` | no | Optimize for time (FAST) or accuracy (FULL). |
| `forTransfer` | query | `boolean` | no | Whether to include domains available for transfer. |
