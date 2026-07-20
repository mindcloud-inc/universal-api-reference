# Sync Account with LOBSTR.IO

Synchronizes an account in LOBSTR.IO using cookies.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/cookies`
- **Base URL:** `https://api.lobstr.io`
- **Official documentation:** [Sync Account](https://docs.lobstr.io/docs/sync-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cookies` | body | `object` | yes | Cookie values required for the selected account type. |
| `type` | body | `string` | yes | The account type identifier to synchronize. |
