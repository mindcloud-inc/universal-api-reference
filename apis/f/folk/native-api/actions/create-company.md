# Create Company with folk

Creates a new company in folk.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/companies`
- **Base URL:** `https://api.folk.app`
- **Official documentation:** [Create Company](https://developer.folk.app/api-reference/companies/create-a-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | An optional description for the company. |
| `name` | body | `string` | yes | The company name. |
