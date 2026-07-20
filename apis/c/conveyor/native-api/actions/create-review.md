# Create Review with Conveyor

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/reviews`
- **Base URL:** `https://api.conveyor.com/api`
- **Official documentation:** [Create Review](https://docs.conveyor.com/reference/post-reviews)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Reviewer email address. |
| `iteration_vm_id` | query | `string` | no | Iteration vendor-management identifier. |
| `question_group_id` | query | `string` | no | Question group identifier. |
| `vendor_vm_id` | query | `string` | no | Vendor-management vendor identifier. |
| `vendor_name` | query | `string` | yes | Vendor name for the review. |
