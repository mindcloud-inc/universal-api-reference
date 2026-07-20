# Delete Job with NeverBounce

Deletes an existing verification job from NeverBounce.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/delete`
- **Base URL:** `https://api.neverbounce.com/v4.2`
- **Official documentation:** [Delete Job](https://developers.neverbounce.com/reference/jobs-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | body | `number` | yes | NeverBounce job identifier. |
