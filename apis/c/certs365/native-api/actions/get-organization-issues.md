# Get Organization Issues with Certs 365

Retrieves organization-issued certificates from Certs 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/get-organization-issues`
- **Base URL:** `https://api1.certs365.io`
- **Official documentation:** [Get Organization Issues](https://help.certs365.io/documentation/fetching-upload-request-details/get-certification-issued-with-given-name-by-issuer-under-the-organization-mobile-application/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | body | `string` | yes | Organization name to search within. |
| `name` | body | `string` | yes | Student or candidate name to search for. |
