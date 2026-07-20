# Create Campaign with JmpTo

Creates a campaign in JmpTo.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign/add`
- **Base URL:** `https://jmpto.net/api`
- **Official documentation:** [Create Campaign](https://jmpto.net/developers#create-a-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Campaign name. |
| `slug` | body | `string` | no | Rotator slug. |
| `public` | body | `boolean` | no | Campaign access flag. |
