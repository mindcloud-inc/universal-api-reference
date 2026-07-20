# Create Job with ServiceTitan

## Endpoint

- **Method:** `POST`
- **Path:** `jpm/v2/tenant/{tenant}/jobs`
- **Base URL:** `https://{baseUrl}/`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appointments[].start` | body | `string` | no | — |
| `customerId` | body | `number` | yes | — |
| `customFields[].typeId` | body | `number` | no | — |
| `externalData.applicationGuid` | body | `string` | no | — |
| `externalData.externalData[].key` | body | `string` | no | — |
| `appointments[].end` | body | `string` | no | — |
| `customFields[].value` | body | `string` | no | — |
| `externalData.externalData[]` | body | `array` | no | — |
| `externalData.externalData[].value` | body | `string` | no | — |
| `locationId` | body | `number` | yes | — |
| `appointments[].arrivalWindowStart` | body | `string` | no | — |
| `projectId` | body | `number` | no | — |
| `appointments[].arrivalWindowEnd` | body | `string` | no | — |
| `businessUnitId` | body | `number` | yes | — |
| `appointments[].technicianIds` | body | `string` | no | Send multiple values as a array. |
| `jobTypeId` | body | `number` | yes | — |
| `priority` | body | `string` | yes | — |
| `campaignId` | body | `number` | no | — |
| `summary` | body | `string` | no | — |
| `customerPo` | body | `string` | no | — |
| `customFields[]` | body | `array` | no | — |
| `summary` | body | `string` | no | — |
| `appointments[]` | body | `array` | no | — |
| `jobStatus` | body | `string` | no | — |
| `externalData` | body | `object` | no | — |
