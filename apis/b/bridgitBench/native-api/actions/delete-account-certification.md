# Delete Account Certification with Bridgit Bench

## Endpoint

- **Method:** `DELETE`
- **Path:** `/rp/api/v1/accounts/:accountId/certifications/:id`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Delete Account Certification](https://developers.gobridgit.com/reference/accountcertifications_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | Id of the certification to remove |
