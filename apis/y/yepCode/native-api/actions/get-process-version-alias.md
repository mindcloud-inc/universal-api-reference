# Get process version alias with YepCode

Retrieves a process version alias from YepCode.

## Endpoint

- **Method:** `GET`
- **Path:** `/processes/:processId/aliases/:aliasId`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Get process version alias](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/getProcessVersionAlias)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processId` | path | `string` | yes | Process ID whose alias you want to retrieve. |
| `aliasId` | path | `string` | yes | Alias ID to retrieve. |
