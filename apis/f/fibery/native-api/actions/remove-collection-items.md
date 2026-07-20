# Remove Collection Items with Fibery

Removes collection items from an entity in Fibery.

## Endpoint

- **Method:** `POST`
- **Path:** `/commands`
- **Base URL:** `https://{account}.fibery.io/api`
- **Official documentation:** [Remove Collection Items](https://the.fibery.io/@public/User_Guide/Guide/Entity-API-264)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Fibery type that owns the collection field. |
| `field` | body | `string` | yes | Collection field name on the source entity. |
| `entity` | body | `object` | yes | Source entity reference that owns the collection field. |
| `items[]` | body | `array<object>` | yes | Collection items to remove. |
