# Create Comment with Streak

Creates a new comment in Streak.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/boxes/:boxKey/comments`
- **Base URL:** `https://api.streak.com`
- **Official documentation:** [Create Comment](https://streak.readme.io/reference/create-a-comment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `boxKey` | path | `string` | yes |
| `message` | body | `string` | yes |
