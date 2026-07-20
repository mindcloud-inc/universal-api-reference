# Query Records with Instant

Retrieves records from Instant with an InstaQL query.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/query`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Query Records](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | yes | InstaQL query object to run. |
