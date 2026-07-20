# Add user to project with Testomato

Adds a user to a Testomato project.

## Endpoint

- **Method:** `POST`
- **Path:** `/project/:id/users`
- **Base URL:** `https://testomato.com/api`
- **Official documentation:** [Add user to project](https://help.testomato.com/api/add-user-to-project)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `email` | body | `string` | yes |
| `role` | body | `number` | yes |
