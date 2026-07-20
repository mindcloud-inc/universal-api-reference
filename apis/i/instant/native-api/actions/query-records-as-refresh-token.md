# Query Records As Refresh Token with Instant

Retrieves records from Instant as a user by refresh token.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/query`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Query Records As Refresh Token](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | yes | InstaQL query object to run. |
| `asToken` | body | `string` | yes | Refresh token to impersonate for permission-aware queries. |
