# Update Deal with RAYNET CRM

## Endpoint

- **Method:** `POST`
- **Path:** `businessCase/:businessCaseId/`
- **Base URL:** `https://app.raynetcrm.com/api/v2/`
- **Official documentation:** [Update Deal](https://app.raynetcrm.com/api/doc/index-en.html#tag/Deals/operation/businessCaseEdit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessCaseId` | path | `string` | yes | Raynet deal identifier. |
| `company` | body | `number` | no | Linked company identifier. |
| `description` | body | `string` | no | Deal description. |
| `estimatedValue` | body | `number` | no | Estimated deal value. |
| `name` | body | `string` | no | Deal name. |
| `totalAmount` | body | `number` | no | Deal total amount. |
