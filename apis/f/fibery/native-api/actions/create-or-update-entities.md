# Create Or Update Entities with Fibery

Creates or updates entities in Fibery.

## Endpoint

- **Method:** `POST`
- **Path:** `/commands`
- **Base URL:** `https://{account}.fibery.io/api`
- **Official documentation:** [Create Or Update Entities](https://the.fibery.io/@public/User_Guide/Guide/Entity-API-264)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Fibery type name shared by all entities in the batch. |
| `entities[]` | body | `array<object>` | yes | Array of entities to create or update. |
| `conflictField` | body | `string` | no | Field used to match existing entities when an item has no Fibery ID. |
| `conflictAction` | body | `string` | no | What Fibery should do on conflict, for example `merge` or `skip`. |
