# Search Authorization Analytics with Satori Cyber

Finds authorization analytics records in Satori Cyber.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/authorization-analytics/:accountId/query`
- **Base URL:** `https://app.satoricyber.com`
- **Official documentation:** [Search Authorization Analytics](https://app.satoricyber.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Satori account ID. |
