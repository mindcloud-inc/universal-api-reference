# Response times with Testomato

Retrieves project response times from Testomato.

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:id/responseTimes`
- **Base URL:** `https://testomato.com/api`
- **Official documentation:** [Response times](https://help.testomato.com/api/response-times)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `start` | query | `date` | yes |
