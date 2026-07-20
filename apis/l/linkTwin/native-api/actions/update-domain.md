# Update Domain with LinkTwin

Updates an existing branded domain in LinkTwin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/domain/:id/update`
- **Base URL:** `https://linktw.in/api`
- **Official documentation:** [Update Domain](https://linktw.in/developers#update-domain)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `redirectroot` | body | `string` | no |
| `redirect404` | body | `string` | no |
