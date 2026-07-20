# Update Role By ID with Coast

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/roles/:roleId`
- **Base URL:** `https://public.coastpay.com`
- **Official documentation:** [Update Role By ID](https://coastpay.com/integrations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roleId` | path | `string` | yes | Coast role ID of the role to update. |
| `name` | body | `string` | no | Updated name for the role. |
| `description` | body | `string` | no | Updated description for the role. |
| `permissions` | body | `object` | no | Updated permissions object for the role. |
