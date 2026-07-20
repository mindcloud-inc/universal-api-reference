# Get Issue Count with Bytesafe

Retrieves an issue count from Bytesafe reports.

## Endpoint

- **Method:** `GET`
- **Path:** `/issues/count`
- **Base URL:** `https://mindcloud.bytesafe.dev/api/v1/`
- **Official documentation:** [Get Issue Count](https://docs.bytesafe.dev/reports/issues-summary/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | yes | Issue status to count, for example OPEN. |
