# Refresh Cookies with LOBSTR.IO

Refreshes account cookies in LOBSTR.IO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/cookies`
- **Base URL:** `https://api.lobstr.io`
- **Official documentation:** [Refresh Cookies](https://docs.lobstr.io/docs/refresh-cookies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account` | body | `string` | yes | The existing account identifier to refresh. |
| `cookies` | body | `object` | yes | Updated cookie values for the existing account. |
| `type` | body | `string` | yes | The account type identifier for the refreshed cookies. |
