# Create Post with Canny

Creates a new post in Canny.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/posts/create`
- **Base URL:** `https://canny.io/api`
- **Official documentation:** [Create Post](https://developers.canny.io/api-reference#create_post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `authorID` | body | `string` | yes |
| `boardID` | body | `string` | yes |
| `title` | body | `string` | yes |
| `details` | body | `string` | yes |
| `categoryID` | body | `string` | no |
| `ownerID` | body | `string` | no |
| `byID` | body | `string` | no |
| `eta` | body | `string` | no |
| `etaPublic` | body | `boolean` | no |
| `imageURLs` | body | `list<string>` | no |
| `customFields` | body | `object` | no |
| `createdAt` | body | `date` | no |
