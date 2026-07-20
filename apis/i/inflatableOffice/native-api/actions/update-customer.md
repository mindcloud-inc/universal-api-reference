# Update Customer with InflatableOffice

Updates an existing customer in InflatableOffice.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/:customerId`
- **Base URL:** `https://rental.software/api6`
- **Official documentation:** [Update Customer](https://rental.software/support/knowledge-base/article/api-customers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cleartags` | body | `boolean` | no | Whether the provided customer tags should replace the existing tags. |
| `customerId` | path | `string` | yes | ID of the customer to update. |
| `custtags` | body | `string` | no | Comma-separated tags to apply to the customer. |
| `notes` | body | `string` | no | Private customer notes. |
| `organization` | body | `string` | no | Updated organization name for the customer. |
