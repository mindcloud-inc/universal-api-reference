# Update Account with NEXT

Updates an existing account in NEXT.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:id`
- **Base URL:** `https://rest.eu-west-1.nextapp.co/v1`
- **Official documentation:** [Update Account](https://developer.nextapp.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The NEXT account ID. |
| `name` | body | `string` | yes | Updated account name. |
| `status` | body | `string` | no | Updated account status. |
