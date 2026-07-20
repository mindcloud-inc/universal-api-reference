# List Versions with AppFollow

Retrieves app version changes from AppFollow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/meta/versions`
- **Base URL:** `https://api.appfollow.io`
- **Official documentation:** [List Versions](https://docs.api.appfollow.io/reference/versions__any_changes_including_meta_data__api_v2_meta_versions_get-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ext_id` | query | `string` | yes | App external ID. |
| `country` | query | `string` | yes | Country code. |
| `lang` | query | `string` | no | Language code. |
| `unique` | query | `number` | no | Unique flag. |
