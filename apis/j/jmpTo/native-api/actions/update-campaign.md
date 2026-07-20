# Update Campaign with JmpTo

Updates an existing campaign in JmpTo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/campaign/:id/update`
- **Base URL:** `https://jmpto.net/api`
- **Official documentation:** [Update Campaign](https://jmpto.net/developers#update-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Campaign ID to update. |
| `slug` | body | `string` | no | Rotator slug. |
| `name` | body | `string` | yes | Campaign name. |
| `public` | body | `boolean` | no | Campaign access flag. |
