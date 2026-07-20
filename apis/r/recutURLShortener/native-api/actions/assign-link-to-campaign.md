# Assign Link To Campaign with Recut URL Shortener

Assigns a link to a campaign in Recut URL Shortener.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign/:campaignid/assign/:linkid`
- **Base URL:** `https://app.recut.in/api`
- **Official documentation:** [Assign Link To Campaign](https://app.recut.in/developers#assign-a-link-to-a-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignid` | path | `number` | yes | Campaign ID. |
| `linkid` | path | `number` | yes | Short link ID. |
