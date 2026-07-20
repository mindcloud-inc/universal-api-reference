# Create Or Update Profile with Reloadify

Creates or updates a profile in Reloadify by email.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/languages/:language_id/profiles`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [Create Or Update Profile](https://app.reloadify.com/api-docs/index.html#/profiles/putV2LanguagesLanguageIdProfiles)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Reloadify language ID. |
| `profile.id` | body | `string` | yes | Profile identifier. |
| `profile.email` | body | `string` | yes | Profile email address. |
