# Update Person Certification with Bridgit Bench

## Endpoint

- **Method:** `PUT`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/certifications/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Update Person Certification](https://developers.gobridgit.com/reference/personcertifications_update)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `personId` | path | `number` | yes | The Person ID |
| `id` | path | `number` | yes | Id of the certification to update |
| `expiryDate` | body | `date` | no | — |
| `certificationDate` | body | `date` | no | — |
| `certificationDescription` | body | `string` | no | Must be no greater than 255 characters. |
