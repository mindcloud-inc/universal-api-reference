# Update User Assigned Locations with Ecotrak

Updates a user's assigned locations in Ecotrak.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/user/:user_id/location`
- **Base URL:** `https://api.ecotrak.com`
- **Official documentation:** [Update User Assigned Locations](https://documenter.getpostman.com/view/19394488/2sAYk8u3FF#customer-user-edit-user-s-assigned-locations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | Ecotrak user ID. |
| `org_ids[]` | body | `array<number>` | yes | Full list of assigned organization IDs. |
