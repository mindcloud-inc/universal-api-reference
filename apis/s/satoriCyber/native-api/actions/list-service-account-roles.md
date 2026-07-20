# List Service Account Roles with Satori Cyber

Retrieves roles for a service account in Satori Cyber.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/service-accounts/:serviceAccountId/roles`
- **Base URL:** `https://app.satoricyber.com`
- **Official documentation:** [List Service Account Roles](https://app.satoricyber.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `serviceAccountId` | path | `string` | yes | Service account identifier. |
