# Change Post Status with Canny

Updates a post status in Canny.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/posts/change_status`
- **Base URL:** `https://canny.io/api`
- **Official documentation:** [Change Post Status](https://developers.canny.io/api-reference#change_post_status)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `changerID` | body | `string` | yes |
| `postID` | body | `string` | yes |
| `status` | body | `string` | yes |
| `shouldNotifyVoters` | body | `boolean` | yes |
| `commentValue` | body | `string` | no |
| `commentImageURLs` | body | `list<string>` | no |
