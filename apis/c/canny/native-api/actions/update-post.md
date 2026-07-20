# Update Post with Canny

Updates an existing post in Canny.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/posts/update`
- **Base URL:** `https://canny.io/api`
- **Official documentation:** [Update Post](https://developers.canny.io/api-reference#update_post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `postID` | body | `string` | yes |
| `title` | body | `string` | no |
| `details` | body | `string` | no |
| `eta` | body | `string` | no |
| `etaPublic` | body | `boolean` | no |
| `imageURLs` | body | `list<string>` | no |
| `customFields` | body | `object` | no |
