# Configure App Authentication with Shuffler

Updates an app authentication in Shuffler.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/authentication/{authenticationId}/config`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Configure App Authentication](https://shuffler.io/docs/API#set-authentication-everywhere)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | body | `string` | yes | Configuration action such as assign_everywhere or suborg_distribute. |
| `authenticationId` | path | `string` | yes | Authentication Id path parameter. |
