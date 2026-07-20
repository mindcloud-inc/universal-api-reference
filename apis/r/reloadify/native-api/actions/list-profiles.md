# List Profiles with Reloadify

Retrieves profiles from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/profiles`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [List Profiles](https://app.reloadify.com/api-docs/index.html#/profiles/getV2LanguagesLanguageIdProfiles)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_after` | query | `string` | no | Only return profiles created after this datetime. |
| `created_before` | query | `string` | no | Only return profiles created before this datetime. |
| `emails[]` | query | `string` | no | Only return profiles matching these email addresses. |
| `language_id` | path | `string` | yes | Language ID from the Reloadify language resource. |
| `updated_after` | query | `string` | no | Only return profiles updated after this datetime. |
| `updated_before` | query | `string` | no | Only return profiles updated before this datetime. |
