# Create Cost Center with e-Boekhouden.nl

Creates a new cost center in e-Boekhouden.nl.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/costcenter`
- **Base URL:** `https://api.e-boekhouden.nl`
- **API:** rest
- **Official documentation:** [Create Cost Center](https://api.e-boekhouden.nl/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | The description of the cost center. Error codes COST_003 Cost center description is required. COST_004 Cost center description is too long. COST_005 Cost center with this name already exists on this level of the tree. COST_011 Cost center fullPath is too long. COST_012 Cost center description has invalid characters. Maximum length: 50. |
| `parentId` | body | `number` | no | The parent ID of the cost center. Error codes COST_005 Cost center with this name already exists on this level of the tree. COST_006 Cost center parent id cannot be changed. COST_007 Cost center parent is not active. COST_008 Cost center parent not found. |
| `active` | body | `boolean` | no | Whether the cost center is active. Error codes COST_007 Cost center parent is not active. |
