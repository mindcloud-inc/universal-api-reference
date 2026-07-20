# List Customers, Attributes, and Devices with Customer.io

Retrieves customers, attributes, and devices from Customer.io by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/customers/attributes`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [List Customers, Attributes, and Devices](https://docs.customer.io/integrations/api/app/#tag/Customers/operation/getPeopleById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes | An array of 1 to 100 customer IDs. |
