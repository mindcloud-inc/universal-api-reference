# List Mock Server Call Logs with Postman

Retrieves call logs for a mock server in Postman.

## Endpoint

- **Method:** `GET`
- **Path:** `/mocks/:mockId/call-logs`
- **Base URL:** `https://api.getpostman.com`
- **Official documentation:** [List Mock Server Call Logs](https://www.postman.com/postman/postman-public-workspace/request/5a1zzxz/get-a-mock-server-s-call-logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mockId` | path | `string` | yes | The mock server's ID. |
