# Get API token with Testomato

Generates an API token in Testomato.

## Endpoint

- **Method:** `POST`
- **Path:** `/authenticate`
- **Base URL:** `https://testomato.com/api`
- **Official documentation:** [Get API token](https://help.testomato.com/api/get-api-token)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `password` | body | `string` | yes |
