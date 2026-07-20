# Create Campaign with Recut URL Shortener

Creates a campaign in Recut URL Shortener.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign/add`
- **Base URL:** `https://app.recut.in/api`
- **Official documentation:** [Create Campaign](https://app.recut.in/developers#create-a-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Campaign name. |
| `slug` | body | `string` | no | Rotator slug. |
| `public` | body | `boolean` | no | Whether the campaign is publicly accessible. |
