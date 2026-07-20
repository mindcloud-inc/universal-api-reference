# List Domains with Release0

Retrieves custom domains from a Release0 workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/domains`
- **Base URL:** `https://release0.com/api`
- **Official documentation:** [List Domains](https://docs.release0.com/workspace/customDomains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | query | `string` | yes | The workspace ID to list domains for. |
