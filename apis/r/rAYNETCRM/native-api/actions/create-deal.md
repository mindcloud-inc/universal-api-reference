# Create Deal with RAYNET CRM

## Endpoint

- **Method:** `PUT`
- **Path:** `businessCase/`
- **Base URL:** `https://app.raynetcrm.com/api/v2/`
- **Official documentation:** [Create Deal](https://app.raynetcrm.com/api/doc/index-en.html#tag/Deals/operation/businessCaseInsert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `number` | yes | Existing Raynet company identifier. |
| `description` | body | `string` | no | Deal description. |
| `estimatedValue` | body | `number` | no | Estimated deal value. |
| `name` | body | `string` | yes | Deal name. |
| `totalAmount` | body | `number` | no | Deal total amount. |
