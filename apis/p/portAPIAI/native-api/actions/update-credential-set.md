# Update Credential Set with Port API AI

Updates a credential set in Port.

## Endpoint

- **Method:** `PUT`
- **Path:** `/apps/:id`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update Credential Set](https://docs.port.io/api-reference/change-the-name-of-a-credentials-set)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Port credential set identifier. |
| `name` | body | `string` | yes | Credential set name |
