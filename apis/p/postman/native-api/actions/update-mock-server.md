# Update Mock Server with Postman

Updates an existing mock server in Postman.

## Endpoint

- **Method:** `PUT`
- **Path:** `/mocks/:mockId`
- **Base URL:** `https://api.getpostman.com`
- **Official documentation:** [Update Mock Server](https://www.postman.com/postman/postman-public-workspace/request/ursyofi/update-a-mock-server)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mockId` | path | `string` | yes | The mock server's ID. |
| `mock.name` | body | `string` | no | — |
