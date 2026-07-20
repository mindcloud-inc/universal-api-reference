# Update Organization with Port API AI

Updates organization details in Port.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/organization`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update Organization](https://docs.port.io/api-reference/update-organization-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Organization description |
| `name` | body | `string` | yes | Organization name |
