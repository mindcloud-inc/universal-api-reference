# Show Client with Invoice Ninja

## Endpoint

- **Method:** `GET`
- **Path:** `/clients/:id`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Show Client](https://api-docs.invoicing.co/#tag/clients/operation/showClient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Invoice Ninja hashed client ID. |
| `include` | query | `string` | no | Optional related resources to include, comma separated. |
