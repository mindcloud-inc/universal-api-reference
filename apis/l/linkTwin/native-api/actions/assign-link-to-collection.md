# Assign Link To Collection with LinkTwin

Assigns a link to a collection in LinkTwin.

## Endpoint

- **Method:** `POST`
- **Path:** `/collection/:collectionid/assign/:itemid`
- **Base URL:** `https://linktw.in/api`
- **Official documentation:** [Assign Link To Collection](https://linktw.in/developers#assign-a-link-to-a-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionid` | path | `string` | yes | Collection ID. |
| `itemid` | path | `string` | yes | Link ID. |
