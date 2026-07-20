# Get Datastore Key with Shuffler

Retrieves a datastore key from Shuffler.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/{orgId}/get_cache`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Get Datastore Key](https://shuffler.io/docs/API#get-a-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | no | Optional datastore category. |
| `key` | body | `string` | yes | Datastore key. |
| `orgId` | path | `string` | yes | Org Id path parameter. |
