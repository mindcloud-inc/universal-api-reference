# Set Datastore Key with Shuffler

Creates a datastore key in Shuffler.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/{orgId}/set_cache`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Set Datastore Key](https://shuffler.io/docs/API#add-a-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | no | Optional datastore category. |
| `key` | body | `string` | yes | Datastore key. |
| `orgId` | path | `string` | yes | Org Id path parameter. |
| `value` | body | `string` | yes | Datastore value. |
