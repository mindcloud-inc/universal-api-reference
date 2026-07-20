# Create Mock Server with Postman

Creates a new mock server in Postman.

## Endpoint

- **Method:** `POST`
- **Path:** `/mocks`
- **Base URL:** `https://api.getpostman.com`
- **Official documentation:** [Create Mock Server](https://www.postman.com/postman/postman-public-workspace/request/5y0q4k4/create-a-mock-server)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace` | query | `string` | no |
| `mock.name` | body | `string` | yes |
| `mock.collection` | body | `string` | yes |
| `mock.environment` | body | `string` | no |
| `mock.private` | body | `boolean` | no |
