# Create Comment with Canny

Creates a new comment in Canny.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/comments/create`
- **Base URL:** `https://canny.io/api`
- **Official documentation:** [Create Comment](https://developers.canny.io/api-reference#create_comment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `authorID` | body | `string` | yes |
| `postID` | body | `string` | yes |
| `value` | body | `string` | yes |
| `createdAt` | body | `date` | no |
| `imageURLs` | body | `list<string>` | no |
| `internal` | body | `boolean` | no |
| `parentID` | body | `string` | no |
| `shouldNotifyVoters` | body | `boolean` | no |
