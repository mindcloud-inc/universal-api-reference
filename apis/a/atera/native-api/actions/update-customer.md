# Update customer with Atera

Updates an existing customer in Atera.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v3/customers/:customerId`
- **Base URL:** `https://app.atera.com`
- **Official documentation:** [Update customer](https://app.atera.com/apidocs#!/Customer/Customer_Put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Address` | body | `string` | no | Street address. |
| `BusinessNumber` | body | `string` | no | Business number. |
| `City` | body | `string` | no | City. |
| `Country` | body | `string` | no | Country. |
| `customerId` | path | `number` | yes | System customer ID. |
| `CustomerName` | body | `string` | no | Customer name. |
| `Domain` | body | `string` | no | Customer domain. |
| `Fax` | body | `string` | no | Fax number. |
| `Latitude` | body | `number` | no | Latitude. |
| `Links` | body | `string` | no | Related links. |
| `Longitude` | body | `number` | no | Longitude. |
| `Notes` | body | `string` | no | Customer notes. |
| `Phone` | body | `string` | no | Phone number. |
| `State` | body | `string` | no | State or region. |
| `ZipCodeStr` | body | `string` | no | ZIP or postal code. |
