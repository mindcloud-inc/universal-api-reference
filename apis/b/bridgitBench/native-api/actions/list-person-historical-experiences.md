# List Person Historical Experiences with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Person Historical Experiences](https://developers.gobridgit.com/reference/personhistoricalexperiences_getall)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The account ID. |
| `personId` | path | `number` | yes | The person ID. |
