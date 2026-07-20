# Duplicate Site with Makeswift

Creates a copy of a site in Makeswift.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/sites/:siteId/duplicate`
- **Base URL:** `https://api.makeswift.com`
- **Official documentation:** [Duplicate Site](https://docs.makeswift.com/developer/reference/api/sites/duplicate-site)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | The source site ID to duplicate. |
| `name` | body | `string` | yes | Name for the duplicated site. |
