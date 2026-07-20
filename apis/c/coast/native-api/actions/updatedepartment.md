# Update Department By ID with Coast

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/departments/:departmentId`
- **Base URL:** `https://public.coastpay.com`
- **Official documentation:** [Update Department By ID](https://coastpay.com/integrations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `departmentId` | path | `string` | yes | Coast department ID of the department to update. |
| `name` | body | `string` | no | Updated name for the department. |
