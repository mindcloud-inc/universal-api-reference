# List Issues with Bytesafe

Retrieves issues from your Bytesafe workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/issues`
- **Base URL:** `https://mindcloud.bytesafe.dev/api/v1/`
- **Official documentation:** [List Issues](https://docs.bytesafe.dev/issues/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `registry` | query | `string` | yes | Registry ID or name to filter issues. |
| `status` | query | `string` | yes | Issue status to filter by. |
