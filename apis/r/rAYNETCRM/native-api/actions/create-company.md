# Create Company with RAYNET CRM

## Endpoint

- **Method:** `PUT`
- **Path:** `company/`
- **Base URL:** `https://app.raynetcrm.com/api/v2/`
- **Official documentation:** [Create Company](https://app.raynetcrm.com/api/doc/index-en.html#tag/Accounts/operation/companyInsert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | [Name] |
| `rating` | body | `string` | yes | [Rating] |
| `state` | body | `string` | yes | [Status] |
| `role` | body | `string` | yes | [Relationship] |
| `notice` | body | `string` | no | [Note to account] |
| `regNumber` | body | `string` | no | [ID no.] |
| `taxNumber` | body | `string` | no | [Tax ID no.] |
