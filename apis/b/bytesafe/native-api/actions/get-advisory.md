# Get Advisory with Bytesafe

Retrieves a vulnerability advisory from Bytesafe.

## Endpoint

- **Method:** `GET`
- **Path:** `/artifacts/advisory/:advisoryId`
- **Base URL:** `https://mindcloud.bytesafe.dev/api/v1/`
- **Official documentation:** [Get Advisory](https://docs.bytesafe.dev/issues/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `advisoryId` | path | `string` | yes | The advisory identifier. |
