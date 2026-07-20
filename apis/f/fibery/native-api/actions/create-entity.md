# Create Entity with Fibery

Creates a new entity in Fibery.

## Endpoint

- **Method:** `POST`
- **Path:** `/commands`
- **Base URL:** `https://{account}.fibery.io/api`
- **Official documentation:** [Create Entity](https://the.fibery.io/@public/User_Guide/Guide/Entity-API-264)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Fibery type name, for example `Project Tracking/Task`. |
| `entity` | body | `object` | yes | Entity object to create. |
