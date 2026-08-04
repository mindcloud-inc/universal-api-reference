# Update Job with ServiceTitan

Updates an existing job in ServiceTitan.

## Endpoint

- **Method:** `PATCH`
- **Path:** `jpm/v2/tenant/{tenant}/jobs/:jobId`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Update Job](https://developer.servicetitan.io/docs/apis/tenant-jpm-v2/endpoints/Jobs_Update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `number` | yes | The ServiceTitan job ID to update. |
| `customerId` | body | `number` | no | ID of the job's customer. |
| `locationId` | body | `number` | no | ID of the job's location. |
| `businessUnitId` | body | `number` | no | ID of the job's business unit. |
| `jobTypeId` | body | `number` | no | ID of the job type. |
| `priority` | body | `string` | no | Job priority value accepted by ServiceTitan. |
| `campaignId` | body | `number` | no | ID of the campaign associated with the job. |
| `summary` | body | `string` | no | Job summary. ServiceTitan accepts HTML. |
| `customerPo` | body | `string` | no | Customer purchase order value. |
| `jobGeneratedLeadSource` | body | `object<object>` | no | Optional generated lead source object containing a job ID and/or employee ID. |
| `jobGeneratedLeadSource.jobId` | body | `number` | no | ID of the job from which this job was generated. |
| `jobGeneratedLeadSource.employeeId` | body | `number` | no | ID of the office user or technician that generated the lead. |
| `shouldUpdateInvoiceItems` | body | `boolean` | no | When true, also updates the business unit on invoice items for the job. |
| `customFields[]` | body | `array<object>` | no | Complete custom-field array. Sending this field replaces all existing custom-field values on the job. |
| `customFields[].typeId` | body | `number` | no | ID of the custom field. |
| `customFields[].value` | body | `string` | no | Value of the custom field. |
| `tagTypeIds[]` | body | `array<number>` | no | Complete tag type ID array. Sending this field replaces all existing tags on the job. |
| `externalData` | body | `object<object>` | no | External data update object. applicationGuid and externalData entries are required when this object is provided. |
| `externalData.patchMode` | body | `list` | no | Replace removes omitted keys; Merge changes only supplied keys. Accepted values: `Merge`, `Replace`. |
| `externalData.applicationGuid` | body | `string` | no | Application GUID that owns the external data. |
| `externalData.externalData[]` | body | `array<object>` | no | External data entries containing key and value. |
| `externalData.externalData[].key` | body | `string` | no | External data key. |
| `externalData.externalData[].value` | body | `string` | no | External data value. A null value deletes the key when using Merge. |
| `soldById` | body | `number` | no | ID of the technician credited with selling the job. |
| `isAutoDispatched` | body | `boolean` | no | Whether Dispatch Pro is enabled for this job. |
| `summaryOfWork` | body | `string` | no | Summary of completed work. This ServiceTitan field is available only to enabled accounts. |
| `noCharge` | body | `boolean` | no | Whether the job is a no-charge job. |
