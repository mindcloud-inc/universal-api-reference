# Create Job with ServiceTrade

Creates a new job in ServiceTrade.

## Endpoint

- **Method:** `POST`
- **Path:** `job`
- **Base URL:** `https://api.servicetrade.com/api`
- **Official documentation:** [Create Job](https://api.servicetrade.com/api/docs#resource-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationId` | body | `number` | yes | Location where the job is performed. |
| `vendorId` | body | `number` | yes | Vendor company performing the work. |
| `type` | body | `string` | yes | Job type to create. |
| `customName` | body | `string` | no | Optional user-facing job name. |
| `description` | body | `string` | no | Optional job description. |
