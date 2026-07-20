# Create Customer with Qualiobee

Creates a new customer in Qualiobee.

## Endpoint

- **Method:** `POST`
- **Path:** `/:organizationUuid/customer`
- **Base URL:** `https://app.qualiobee.fr/api`
- **Official documentation:** [Create Customer](https://app.qualiobee.fr/api/doc/#/Customer/PublicCustomerController_createOne)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationUuid` | path | `string` | yes | The Qualiobee organization UUID used in the request path |
| `name` | body | `string` | yes | The name of the company or the full name of the individual |
| `firstName` | body | `string` | yes | The first name of the referent in the company or the first name of the individual |
| `lastName` | body | `string` | yes | The last name of the referent in the company or the last name of the individual |
| `email` | body | `string` | yes | The email of the referent in the company or the email of the individual |
| `externalId` | body | `string` | no | Optional external identifier for the seeded customer |
| `phoneNumber` | body | `string` | no | The phone number of the referent in the company or the phone number of the individual |
| `siret` | body | `string` | no | The SIRET of the company |
| `naf` | body | `string` | no | The NAF code of the company |
| `note` | body | `string` | no | Some notes to save more details about the customer |
| `isIndividual` | body | `boolean` | no | Whether the customer is a company or an individual |
| `isSoloLearner` | body | `boolean` | no | If true, creates a learner with the customer referent's data |
| `location.addressLine1` | body | `string` | no | The first part of the address |
| `location.addressLine2` | body | `string` | no | The second part of the address |
| `location.postCode` | body | `string` | no | The postal code |
| `location.city` | body | `string` | no | The city |
| `location.country` | body | `string` | no | The country |
