# Update Company with RAYNET CRM

## Endpoint

- **Method:** `POST`
- **Path:** `company/:companyId/`
- **Base URL:** `https://app.raynetcrm.com/api/v2/`
- **Official documentation:** [Update Company](https://app.raynetcrm.com/api/doc/index-en.html#tag/Accounts/operation/companyEdit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | Raynet company identifier. |
| `name` | body | `string` | no | [Name] |
| `rating` | body | `string` | no | [Rating] |
| `state` | body | `string` | no | [Status] |
| `role` | body | `string` | no | [Relationship] |
| `notice` | body | `string` | no | [Note to account] |
| `regNumber` | body | `string` | no | [ID no.] |
| `taxNumber` | body | `string` | no | [Tax ID no.] |
