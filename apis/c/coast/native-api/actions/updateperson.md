# Update Person By ID with Coast

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/people/:personId`
- **Base URL:** `https://public.coastpay.com`
- **Official documentation:** [Update Person By ID](https://coastpay.com/integrations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personId` | path | `string` | yes | Coast person ID of the person to update. |
| `active` | body | `boolean` | no | Whether the person is active in Coast. |
| `firstName` | body | `string` | no | Updated first name for the person. |
| `lastName` | body | `string` | no | Updated last name for the person. |
| `email` | body | `string` | no | Updated email address for the person. |
| `mobilePhone` | body | `string` | no | Updated mobile phone number for the person. |
| `locationId` | body | `string` | no | Coast location ID to assign to the person. |
| `departmentId` | body | `string` | no | Coast department ID to assign to the person. |
| `roleId` | body | `string` | no | Coast role ID to assign to the person. |
| `access` | body | `string` | no | Updated access settings for the person. |
| `policyId` | body | `string` | no | Coast policy ID to assign to the person. |
| `security` | body | `string` | no | Updated security settings for the person. |
| `assignedVehicleId` | body | `string` | no | Coast vehicle ID to assign to the person. |
