# Uptime with Testomato

Retrieves project uptime data from Testomato.

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:id/uptime`
- **Base URL:** `https://testomato.com/api`
- **Official documentation:** [Uptime](https://help.testomato.com/api/uptime)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `start` | query | `date` | yes |
