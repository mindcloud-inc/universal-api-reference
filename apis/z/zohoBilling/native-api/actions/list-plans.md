# List Plans with Zoho Billing

## Endpoint

- **Method:** `GET`
- **Path:** `/plans`
- **Base URL:** `{api_domain}/billing/v1`
- **Official documentation:** [List Plans](https://www.zoho.com/billing/api/v1/plans/#list-all-plans)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter_by` | query | `string` | no | Filter plans by status, for example `PlanStatus.ACTIVE`. |
| `product_id` | query | `string` | no | Filter plans to one product. |
