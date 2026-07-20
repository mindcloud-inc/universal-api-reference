# Enrich Profile with DataForB2B

Retrieves enriched profile data from DataForB2B.

## Endpoint

- **Method:** `POST`
- **Path:** `/enrich/profile`
- **Base URL:** `https://api.dataforb2b.ai`
- **Official documentation:** [Enrich Profile](https://docs.dataforb2b.ai/api-reference/enrich-profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile_identifier` | body | `string` | yes | Profile URL or profile ID to enrich. |
| `enrich_profile` | body | `boolean` | no | Whether to fetch the full profile object. |
| `enrich_work_email` | body | `boolean` | no | Whether to enrich the work email. |
