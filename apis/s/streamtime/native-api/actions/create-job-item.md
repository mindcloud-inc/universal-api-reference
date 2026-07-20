# Create Job Item with Streamtime

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/:job_id/job_items`
- **Base URL:** `https://api.streamtime.net/v2`
- **Official documentation:** [Create Job Item](https://api.streamtime.net/v2/swagger#/Jobs/createJobItem)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `number` | yes | Job ID |
| `jobPhaseId` | body | `number` | yes | Job phase ID |
| `jobItemStatus` | body | `object` | no | Status of a Job item. |
| `jobItemStatus.id` | body | `number` | yes | Job Item Status ID (1=Planning, 4=Scheduled, 2=Complete, 3=Deleted) |
| `name` | body | `string` | yes | Job item name |
| `description` | body | `string` | no | Job item description |
| `sellRate` | body | `number` | no | Explicit sell rate in job currency (if provided) |
| `costingMethod` | body | `object` | no | Consting Method |
| `costingMethod.id` | body | `number` | yes | Consting Method ID (1=Item, 2=People, 3=Fixed Price Calculated Sell, 4=Fixed Price User Sell) |
| `isBillable` | body | `boolean` | yes | Is this job item billable |
| `timeAllocationMethod` | body | `object` | no | How the time of an item is allocated, whether as a bucket that is shared amongst all users or individually assigned to each user. |
| `timeAllocationMethod.id` | body | `number` | yes | Time Allocation Method ID (1=Item, 2=People) |
| `totalPlannedMinutes` | body | `number` | no | Total planned minutes for the item |
| `estimatedStartDate` | body | `date` | no | Estimated start date |
| `estimatedEndDate` | body | `date` | no | Estimated end date |
| `completedDate` | body | `date` | no | Completion date |
