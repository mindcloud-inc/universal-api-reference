# Run TikTok Profile Extractor with Botster

Creates a Botster TikTok profile extraction job.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/tiktok-profile-extractor`
- **Base URL:** `https://botster.io/api/v2`
- **Official documentation:** [Run TikTok Profile Extractor](https://botster.io/bots/tiktok-profile-extractor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cron` | body | `string` | no | Cron schedule for periodic execution. |
| `input` | body | `string` | yes | Profiles. |
