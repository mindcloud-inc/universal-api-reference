# Query Records As Email with Instant

Retrieves records from Instant as a user by email.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/query`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Query Records As Email](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | yes | InstaQL query object to run. |
| `asEmail` | body | `string` | yes | User email to impersonate for permission-aware queries. |
