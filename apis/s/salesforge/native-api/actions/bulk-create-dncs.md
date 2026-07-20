# Bulk Create DNCs with Salesforge

Creates DNC entries in bulk in Salesforge.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v2/workspaces/:workspaceID/dnc/bulk`
- **Base URL:** `https://api.salesforge.ai`
- **Official documentation:** [Bulk Create DNCs](https://api.salesforge.ai/public/v2/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceID` | path | `string` | yes |
| `dncs[]` | body | `array<string>` | yes |
