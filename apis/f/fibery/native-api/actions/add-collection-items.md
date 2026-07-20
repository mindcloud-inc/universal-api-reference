# Add Collection Items with Fibery

Adds collection items to an entity in Fibery.

## Endpoint

- **Method:** `POST`
- **Path:** `/commands`
- **Base URL:** `https://{account}.fibery.io/api`
- **Official documentation:** [Add Collection Items](https://the.fibery.io/@public/User_Guide/Guide/Entity-API-264)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Fibery type that owns the collection field. |
| `field` | body | `string` | yes | Collection field name on the source entity. |
| `entity` | body | `object` | yes | Source entity reference that owns the collection field. |
| `items[]` | body | `array<object>` | yes | Collection items to add. |
