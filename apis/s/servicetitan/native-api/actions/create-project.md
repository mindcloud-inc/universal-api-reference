# Create Project with ServiceTitan

## Endpoint

- **Method:** `POST`
- **Path:** `jpm/v2/tenant/{tenant}/projects`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Create Project](https://developer.servicetitan.io/apis/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customFields[].typeId` | body | `number` | no | — |
| `locationId` | body | `number` | no | — |
| `customerId` | body | `number` | no | — |
| `customFields[].value` | body | `string` | no | — |
| `statusId` | body | `number` | no | — |
| `subStatusId` | body | `number` | no | — |
| `customFields[]` | body | `array` | no | — |
| `summary` | body | `string` | no | — |
| `name` | body | `string` | no | — |
| `businessUnitIds` | body | `number` | no | Send multiple values as a array. |
| `projectTypeId` | body | `list` | no | — |
