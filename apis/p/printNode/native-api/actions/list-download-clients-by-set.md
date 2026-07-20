# List Download Clients by Set with PrintNode

Retrieves specific client downloads from PrintNode by ID set.

## Endpoint

- **Method:** `GET`
- **Path:** `/download/clients/:downloadSet`
- **Base URL:** `https://api.printnode.com`
- **Official documentation:** [List Download Clients by Set](https://www.printnode.com/en/docs/api/curl#account-download-management)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `downloadSet` | path | `string` | yes | Comma-separated PrintNode download client IDs. |
