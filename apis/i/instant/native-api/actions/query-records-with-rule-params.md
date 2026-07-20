# Query Records With Rule Params with Instant

Retrieves records from Instant with rule parameters.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/query`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Query Records With Rule Params](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | yes | InstaQL query object to run. |
| `$$ruleParams` | body | `object` | no | Optional rule parameters for permission-aware queries. |
