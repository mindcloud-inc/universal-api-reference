# Delete Person Certification with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/certifications/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Person Certification](https://developers.gobridgit.com/reference/personcertifications_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `personId` | path | `number` | yes | The Person ID |
| `id` | path | `number` | yes | Id of the certification to remove |
