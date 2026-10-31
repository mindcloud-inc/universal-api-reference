# List Account Person Certifications with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/Accounts/:id/person-certifications`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Account Person Certifications](https://developers.gobridgit.com/reference/accounts_querypersoncertifications)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Account ID |
| `personIds` | query | `number` | no | Optional paramater of comma delimited ids for filtering results based on the person IDs provided Send multiple values as a string separated by `,`. |
