# Add Profiles To Monitor with DataForB2B

Adds profiles to monitoring in DataForB2B.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/profiles`
- **Base URL:** `https://api.dataforb2b.ai`
- **Official documentation:** [Add Profiles To Monitor](https://docs.dataforb2b.ai/api-reference/webhooks-add-profiles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile_ids` | body | `object<string>` | yes | Profile URLs or profile IDs to start monitoring. |
