# Get Customer with Qualiobee

Retrieves a customer from Qualiobee.

## Endpoint

- **Method:** `GET`
- **Path:** `/:organizationUuid/customer/:customerUuid`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [Get Customer](https://app.qualiobee.fr/api/doc/#/Customer/PublicCustomerController_getOne)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes | The Qualiobee organization UUID used in the request path |
| `customerUuid` | path | `string` | yes | The uuid of the customer to fetch |
| `relations` | query | `list<string>` | no | Related entities to include in the customer response Send multiple values as a array. |
| `withDeleted` | query | `boolean` | no | Include deleted customer data in the response |
