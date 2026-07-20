# Get Profile with Reloadify

Retrieves a profile from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/profiles/:profile_id`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [Get Profile](https://app.reloadify.com/api-docs/index.html#/profiles/getV2LanguagesLanguageIdProfilesProfileId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Language ID from the Reloadify language resource. |
| `profile_id` | path | `string` | yes | Profile ID. |
