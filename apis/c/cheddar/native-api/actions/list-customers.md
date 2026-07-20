# List Customers with Cheddar

Retrieves customer billing records from Cheddar.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/get/productCode/{productCode}`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [List Customers](https://docs.getcheddar.com/#get-all-customers)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Text search across customer name, company, email, and the last four digits of the credit card. |
| `subscriptionStatus` | query | `string` | no | Filter customers by subscription status: activeOnly or canceledOnly. |
| `planCode` | query | `list<string>` | no | Filter customers by one or more pricing plan codes. Send multiple values as a array. |
| `createdAfterDate` | query | `date` | no | Return customers created on or after this YYYY-MM-DD date. |
| `createdBeforeDate` | query | `date` | no | Return customers created on or before this YYYY-MM-DD date. |
| `canceledAfterDate` | query | `date` | no | Return customers canceled on or after this YYYY-MM-DD date. |
| `canceledBeforeDate` | query | `date` | no | Return customers canceled on or before this YYYY-MM-DD date. |
| `transactedAfterDate` | query | `date` | no | Return customers with transactions on or after this YYYY-MM-DD date. |
| `transactedBeforeDate` | query | `date` | no | Return customers with transactions on or before this YYYY-MM-DD date. |
