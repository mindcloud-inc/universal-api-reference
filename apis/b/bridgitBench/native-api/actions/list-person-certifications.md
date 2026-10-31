# List Person Certifications with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/certifications`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Person Certifications](https://developers.gobridgit.com/reference/personcertifications_query)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `personId` | path | `number` | yes | The Person ID |
| `ids` | query | `number` | no | (Optional) Filters the result to contain person certifications that match the ids passed in. Send multiple values as a array. |
