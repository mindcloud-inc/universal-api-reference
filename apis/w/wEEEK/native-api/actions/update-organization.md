# Update Organization with WEEEK

## Endpoint

- **Method:** `PATCH`
- **Path:** `/crm/organizations/:organizationId`
- **Base URL:** `https://api.weeek.net/public/v1`
- **Official documentation:** [Update Organization](https://developers.weeek.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The organization name. WEEEK required this field during PATCH validation. |
| `organizationId` | path | `string` | yes | The WEEEK organization ID from the organizations API. |
