# Create Job with Streamtime

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs`
- **Base URL:** `https://api.streamtime.net/v2`
- **Official documentation:** [Create Job](https://api.streamtime.net/v2/swagger#/Jobs/createJob)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | body | `number` | yes | Company ID linked to the job. |
| `jobLeadUserId` | body | `number` | no | Job lead user ID |
| `rateCardId` | body | `number` | yes | The id of the rate card used for this job |
| `branchId` | body | `number` | yes | The id of the branch this job belongs to |
| `jobStatus` | body | `object` | no | Status of a Job. |
| `jobStatus.id` | body | `number` | yes | Job Status ID (5=Paused, 1=In Play, 2=Done, 3=Deleted, 4=Archived) |
| `number` | body | `string` | yes | Job number |
| `name` | body | `string` | yes | Job name |
| `purchaseOrderNumber` | body | `string` | no | Client purchase order number |
| `contactId` | body | `number` | yes | The id of the contact this job is being done for |
