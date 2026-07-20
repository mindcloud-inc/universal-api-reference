# Project update with Testomato

Updates an existing project in Testomato.

## Endpoint

- **Method:** `PUT`
- **Path:** `/project/:id`
- **Base URL:** `https://testomato.com/api`
- **Official documentation:** [Project update](https://help.testomato.com/api/project-update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `url` | body | `string` | no |
| `title` | body | `string` | no |
| `period` | body | `string` | no |
| `timeout` | body | `number` | no |
| `delay` | body | `number` | no |
| `sslAlertPeriod` | body | `number` | no |
| `checkDefaultErrors` | body | `boolean` | no |
| `uptimeEnabled` | body | `number` | no |
| `uptimeUrl` | body | `string` | no |
| `userAgent` | body | `string` | no |
