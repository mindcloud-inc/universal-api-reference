# Update Download Clients with PrintNode

Updates specific client downloads in PrintNode.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/download/clients/:downloadSet`
- **Base URL:** `https://api.printnode.com`
- **Official documentation:** [Update Download Clients](https://www.printnode.com/en/docs/api/curl#account-download-management)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `downloadSet` | path | `string` | yes | Comma-separated PrintNode download client IDs. |
| `enabled` | body | `boolean` | yes | Set to true to enable the selected download clients or false to disable them. |
