# Retrieve Customer with GorillaDesk

Retrieves a customer from GorillaDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/:customerId`
- **Base URL:** `https://api.gorilladesk.com/v1`
- **Official documentation:** [Retrieve Customer](https://api.gorilladesk.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | Customer Id |
| `include[]` | query | `array<string>` | no | Send multiple values as a string separated by `,`. |
