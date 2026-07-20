# Assign Link to Campaign with JmpTo

Assigns a link to a campaign in JmpTo.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign/:campaignid/assign/:linkid`
- **Base URL:** `https://jmpto.net/api`
- **Official documentation:** [Assign Link to Campaign](https://jmpto.net/developers#assign-a-link-to-a-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignid` | path | `number` | yes | Campaign ID to assign the link to. |
| `linkid` | path | `number` | yes | Short link ID to assign. |
