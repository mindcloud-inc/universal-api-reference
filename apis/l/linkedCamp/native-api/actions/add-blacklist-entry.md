# Add Blacklist Entry with LinkedCamp

## Endpoint

- **Method:** `POST`
- **Path:** `/blacklists`
- **Base URL:** `https://api.linkedcamp.com`
- **Official documentation:** [Add Blacklist Entry](https://api.linkedcamp.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | body | `string` | yes | Blacklist keyword or value. |
| `type` | body | `string` | yes | Blacklist type: PROFILE_URL, KEYWORD, or JOB_TITLE. |
| `linkedInAccountEmail` | body | `string` | yes | LinkedIn account email for the blacklist entry. |
