# List New Versions with AppFollow

Retrieves new version details from AppFollow.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/meta/versions/whatsnew`
- **Base URL:** `https://api.appfollow.io`
- **Official documentation:** [List New Versions](https://docs.api.appfollow.io/reference/what_s_new__new_versions__api_v2_meta_versions_whatsnew_get-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ext_id` | query | `string` | yes | App external ID. |
| `country` | query | `string` | no | Country code. |
| `lang` | query | `string` | no | Language code. |
| `last_modified` | query | `string` | no | Last modified date. |
