# Bulk Set Datastore Keys with Shuffler

Creates multiple datastore keys in Shuffler.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/datastore`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Bulk Set Datastore Keys](https://shuffler.io/docs/API#add-multiple-keys)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bulk` | query | `boolean` | yes | Set to true for bulk datastore writes. |
