# Upsert Curation Set with Typesense

Creates or updates a curation set in Typesense.

## Endpoint

- **Method:** `PUT`
- **Path:** `/curation_sets/{{name}}`
- **Base URL:** `https://5brh8vz1lictf0jop-1.a2.typesense.net`
- **Official documentation:** [Upsert Curation Set](https://typesense.org/docs/30.0/api/api-keys.html#curation-set-actions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `curationSet` | body | `object` | yes | Curation set JSON body. |
| `name` | path | `string` | yes | Curation set name. |
