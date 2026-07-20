# Convert Lead with RAYNET CRM

## Endpoint

- **Method:** `POST`
- **Path:** `lead/:leadId/convert/`
- **Base URL:** `https://app.raynetcrm.com/api/v2/`
- **Official documentation:** [Convert Lead](https://app.raynetcrm.com/api/doc/index-en.html#tag/Leads/operation/leadConvert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadId` | path | `string` | yes | Raynet lead identifier. |
| `company` | body | `number` | no | existing account ID |
| `person` | body | `number` | no | existing contact ID |
| `businessCase` | body | `number` | no | existing deal ID |
