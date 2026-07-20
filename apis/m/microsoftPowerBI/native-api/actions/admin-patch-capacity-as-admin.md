# Patch Capacity As Admin with Microsoft Power BI

## Endpoint

- **Method:** `PATCH`
- **Path:** `admin/capacities/[:capacityId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Patch Capacity As Admin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/patch-capacity-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `capacityId` | path | `string` | yes | The capacity ID |
| `tenantKeyId` | body | `string` | no | The ID of the encryption key |
