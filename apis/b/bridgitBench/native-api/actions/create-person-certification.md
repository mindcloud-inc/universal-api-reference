# Create Person Certification with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/certifications`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Person Certification](https://developers.gobridgit.com/reference/personcertifications_add)

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
| `certificationId` | body | `number` | yes | — |
| `expiryDate` | body | `date` | no | — |
| `certificationDate` | body | `date` | no | — |
| `certificationDescription` | body | `string` | no | Must be no greater than ResourcePlanning.Contracts.NewPersonCertificationRequest.MaxDescriptionLength characters. |
