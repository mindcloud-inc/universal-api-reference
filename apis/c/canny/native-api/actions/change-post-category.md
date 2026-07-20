# Change Post Category with Canny

Updates a post category in Canny.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/posts/change_category`
- **Base URL:** `https://canny.io/api`
- **Official documentation:** [Change Post Category](https://developers.canny.io/api-reference#change_post_category)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `postID` | body | `string` | yes |
| `categoryID` | body | `string` | no |
