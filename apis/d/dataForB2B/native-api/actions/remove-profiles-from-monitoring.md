# Remove Profiles From Monitoring with DataForB2B

Removes profiles from monitoring in DataForB2B.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/webhooks/profiles`
- **Base URL:** `https://api.dataforb2b.ai`
- **Official documentation:** [Remove Profiles From Monitoring](https://docs.dataforb2b.ai/api-reference/webhooks-remove-profiles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile_ids` | body | `object<string>` | yes | Profile URLs or profile IDs to stop monitoring. |
