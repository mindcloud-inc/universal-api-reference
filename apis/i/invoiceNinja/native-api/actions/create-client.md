# Create Client with Invoice Ninja

## Endpoint

- **Method:** `POST`
- **Path:** `/clients`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Create Client](https://api-docs.invoicing.co/#tag/clients/operation/storeClient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Optional related resources to include, comma separated. |
| `name` | body | `string` | yes | The name of the client company or organization. |
| `country_id` | body | `number` | yes | Country identifier required by the Invoice Ninja client schema. |
| `contacts[0].first_name` | body | `string` | yes | First name for the primary contact. Client contacts must be included on mutating requests. |
| `contacts[0].last_name` | body | `string` | yes | Last name for the primary contact. Client contacts must be included on mutating requests. |
| `contacts[0].email` | body | `string` | yes | Email for the primary contact. Client contacts must be included on mutating requests. |
