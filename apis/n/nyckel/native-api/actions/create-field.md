# Create Field with Nyckel

Creates a new field in Nyckel.

## Endpoint

- **Method:** `POST`
- **Path:** `/functions/:functionId/fields`
- **Base URL:** `https://www.nyckel.com/v1`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Nyckel function identifier. |
| `name` | body | `string` | yes | Field name. |
| `type` | body | `string` | yes | Field type. |
