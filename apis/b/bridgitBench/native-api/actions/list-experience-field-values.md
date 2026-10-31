# List Experience Field Values with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/experience-fields/:experienceFieldId/values`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Experience Field Values](https://developers.gobridgit.com/reference/experiencefieldvalues_query)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `experienceFieldId` | path | `string` | yes | The Experience Field UUID |
| `name` | query | `string` | no | Filter by name with a contains check not exact match |
