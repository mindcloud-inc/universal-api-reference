# List Customers with ReputationLync

Retrieves customers from ReputationLync.

## Endpoint

- **Method:** `POST`
- **Path:** `/listCustomer`
- **Base URL:** `https://reputationlync.com/app/api/customer`
- **Official documentation:** [List Customers](https://documenter.getpostman.com/view/25361963/2s93Xzw2bS#5c16a301-9417-4539-b9c5-dcdf666159ff)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | body | `string` | no | Return a specific customer by ReputationLync customer ID. |
| `location_id` | body | `string` | no | Filter customers by location identifier. |
| `created_after_date` | body | `string` | no | Only return customers created after this date. |
| `created_before_date` | body | `string` | no | Only return customers created before this date. |
| `created_after_id` | body | `string` | no | Only return customers created after this internal record ID. |
| `created_before_id` | body | `string` | no | Only return customers created before this internal record ID. |
