# Create Client with Outlign

Creates a new client in Outlign.

## Endpoint

- **Method:** `POST`
- **Path:** `/clients`
- **Base URL:** `https://go.outlign.co/api/v1`
- **Official documentation:** [Create Client](https://go.outlign.co/api/docs/clients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The client's name or company name |
| `company_id` | body | `number` | yes | ID of the company this client belongs to |
