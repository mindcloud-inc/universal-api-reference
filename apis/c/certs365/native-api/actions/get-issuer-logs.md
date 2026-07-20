# Get Issuer Logs with Certs 365

Retrieves issuer issue logs from Certs 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/get-issuers-log`
- **Base URL:** `https://api1.certs365.io`
- **Official documentation:** [Get Issuer Logs](https://help.certs365.io/documentation/fetching-upload-request-details/get-issues-under-criterion-for-admin-dashboard/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Issuer email address. |
| `queryCode` | body | `number` | yes | Code used to fetch the appropriate log details. |
