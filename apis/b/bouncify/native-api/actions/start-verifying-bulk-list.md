# Start Verifying Bulk List with Bouncify

Starts verifying a bulk email list in Bouncify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/bulk/:job_id`
- **Base URL:** `https://api.bouncify.io/v1`
- **Official documentation:** [Start Verifying Bulk List](https://bouncify.io/docs/api-docs/bulk-validation/start-verifying-bulk-email-list/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Bulk verification job id to start. |
