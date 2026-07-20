# Get Custom Field Details with Qntrl

Retrieves custom field details from Qntrl.

## Endpoint

- **Method:** `GET`
- **Path:** `/[:org_id]/customfield/[:customfield_id]`
- **Base URL:** `https://coreapi.qntrl.com/blueprint/api`
- **Official documentation:** [Get Custom Field Details](https://core.qntrl.com/apidoc.html#CustomFieldsDetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customfield_id` | path | `string` | no | Qntrl custom field ID. |
| `org_id` | path | `string` | no | Qntrl organization ID. |
