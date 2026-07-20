# Update Campaign with Recut URL Shortener

Updates an existing campaign in Recut URL Shortener.

## Endpoint

- **Method:** `PUT`
- **Path:** `/campaign/:id/update`
- **Base URL:** `https://app.recut.in/api`
- **Official documentation:** [Update Campaign](https://app.recut.in/developers#update-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Campaign ID. |
| `name` | body | `string` | yes | Campaign name. |
| `slug` | body | `string` | no | Rotator slug. |
| `public` | body | `boolean` | no | Whether the campaign is publicly accessible. |
