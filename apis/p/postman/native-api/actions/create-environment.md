# Create Environment with Postman

Creates a new environment in Postman.

## Endpoint

- **Method:** `POST`
- **Path:** `/environments`
- **Base URL:** `https://api.getpostman.com`
- **Official documentation:** [Create Environment](https://www.postman.com/postman/utility-flows/request/2g360ay/create-an-environment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace` | query | `string` | no |
| `environment.name` | body | `string` | yes |
