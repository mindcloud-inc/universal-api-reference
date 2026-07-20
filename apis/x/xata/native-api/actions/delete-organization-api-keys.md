# Bulk delete API Keys for an organization with Xata

## Endpoint

- **Method:** `DELETE`
- **Path:** `/organizations/:organizationID/api-keys`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Bulk delete API Keys for an organization](https://xata.io/docs/api-reference/api-keys/bulk-delete-api-keys-for-an-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array` | yes | Array of API key IDs to delete |
| `ids[]` | body | `array` | yes | Array of API key IDs to delete |
| `organizationID` | path | `string` | yes | Unique identifier for a specific organization |
