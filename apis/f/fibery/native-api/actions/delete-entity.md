# Delete Entity with Fibery

Deletes an existing entity from Fibery.

## Endpoint

- **Method:** `POST`
- **Path:** `/commands`
- **Base URL:** `https://{account}.fibery.io/api`
- **Official documentation:** [Delete Entity](https://the.fibery.io/@public/User_Guide/Guide/Entity-API-264)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Fibery type name, for example `Project Tracking/Task`. |
| `entity` | body | `object` | yes | Entity reference to delete. Include the Fibery ID or public ID. |
