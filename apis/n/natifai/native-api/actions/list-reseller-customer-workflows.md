# List Reseller Customer Workflows with Natif.ai

Retrieves workflows for a reseller customer in Natif.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/reseller/customers/[:customerId]/workflows`
- **Base URL:** `https://api.natif.ai`
- **Official documentation:** [List Reseller Customer Workflows](https://api.natif.ai/docs#/Reseller%20User%20Management/get_customer_workflows_reseller_customers__customer_id__workflows_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | UUID of the customer. |
| `locale` | query | `string` | no | Locale/language to use for workflow labels. |
| `limit` | query | `number` | no | Maximum number of workflows to return. |
