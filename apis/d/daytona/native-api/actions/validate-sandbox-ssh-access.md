# Validate Sandbox SSH Access with Daytona

Validates sandbox SSH access in Daytona.

## Endpoint

- **Method:** `GET`
- **Path:** `/sandbox/ssh-access/validate`
- **Base URL:** `https://app.daytona.io/api`
- **Official documentation:** [Validate Sandbox SSH Access](https://www.daytona.io/docs/tools/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | query | `string` | yes | SSH access token to validate. |
