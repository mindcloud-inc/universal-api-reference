# Create or Update Release with ReleaseNotes

Creates or updates a release in ReleaseNotes.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/releases`
- **Base URL:** `https://api.releasenotes.io/api/v1`
- **Official documentation:** [Create or Update Release](https://releasenotes.elevio.help/en/articles/87753-create-update-a-release)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The numeric Project ID shown in ReleaseNotes URLs like /manage/project/1234/releases/4321. |
| `title` | body | `string` | yes | The release title shown to end users. |
| `description` | body | `string` | no | The main body content for the release. |
| `external_id` | body | `string` | no | Optional external identifier. If it matches an existing release, ReleaseNotes updates that release instead of creating a new one. Maximum length: 25. |
| `featured_image` | body | `string` | no | Optional featured image URL for the release. |
| `type` | body | `string` | no | Optional release type. The docs list update, bugfix, and feature. |
| `owner` | body | `string` | no | Optional owner email address for the release. |
| `status` | body | `string` | no | Optional publication status. The docs list published and pending. |
| `private` | body | `boolean` | no | Optional boolean that controls whether the release is private. |
| `released_at` | body | `string` | no | Optional release timestamp using the provider format YYYY-MM-DD h:m:i. |
