# Query Records As Guest with Instant

Retrieves records from Instant with guest permissions.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/query`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Query Records As Guest](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | yes | InstaQL query object to run. |
| `asGuest` | body | `boolean` | no | When true, runs the query with guest permissions. |
