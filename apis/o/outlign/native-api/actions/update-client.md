# Update Client with Outlign

Updates an existing client in Outlign.

## Endpoint

- **Method:** `PUT`
- **Path:** `/clients/:id`
- **Base URL:** `https://go.outlign.co/api/v1`
- **Official documentation:** [Update Client](https://go.outlign.co/api/docs/clients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the client to update |
| `title` | body | `string` | no | Updated client title |
