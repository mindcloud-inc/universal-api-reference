# Find Creator Connected Socials with Influencers.club

Finds verified connected social accounts for a creator in Influencers.club.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/creators/socials/`
- **Base URL:** `https://api-dashboard.influencers.club`
- **Official documentation:** [Find Creator Connected Socials](https://docs.influencers.club/openapi/connected-socials/public_v1_creators_socials_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `platform` | body | `string` | yes | Creator platform (for example instagram). |
| `handle` | body | `string` | yes | Creator handle without @. |
