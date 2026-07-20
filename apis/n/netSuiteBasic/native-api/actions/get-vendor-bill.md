# Get Vendor Bill with NetSuite - Basic

Retrieves details for the vendor bill in NetSuite.

## Endpoint

- **Method:** `GET`
- **Path:** `/record/v1/vendorBill/:id`
- **Base URL:** `https://{accountDomain}.suitetalk.api.netsuite.com/services/rest`
- **Official documentation:** [Get Vendor Bill](https://system.netsuite.com/help/helpcenter/en_US/APIs/REST_API_Browser/record/v1/2025.2/index.html#/definitions/vendorBill)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Internal NetSuite record ID. |
