# Get Latest Client Download with PrintNode

Retrieves the latest client download from PrintNode by operating system.

## Endpoint

- **Method:** `GET`
- **Path:** `/download/client/:operatingSystem`
- **Base URL:** `https://api.printnode.com`
- **Official documentation:** [Get Latest Client Download](https://www.printnode.com/en/docs/api/curl#account-download-management)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `operatingSystem` | path | `string` | yes | Operating system token from the PrintNode download docs. |
