# Deactivate Person with Details with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/Persons/:id/deactivate`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Deactivate Person with Details](https://developers.gobridgit.com/reference/persons_deactivate)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `id` | path | `number` | yes | The Person ID |
| `deactivationReason` | body | `string` | no | Maximum length: 100. |
| `deactivationNotes` | body | `string` | no | Maximum length: 240. |
| `wouldRehire` | body | `boolean` | no | — |
| `employmentEndDate` | body | `date` | no | — |
