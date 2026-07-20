# Publish Post with Ayrshare

Publishes a post to social networks with Ayrshare.

## Endpoint

- **Method:** `POST`
- **Path:** `/post`
- **Base URL:** `https://api.ayrshare.com/api`
- **Official documentation:** [Publish Post](https://www.ayrshare.com/docs/apis/post/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `post` | body | `string` | yes | Text to publish to the selected social platforms. |
| `platforms[]` | body | `array<string>` | yes | Social platforms to publish to. Ayrshare values include twitter, facebook, instagram, linkedin, youtube, tiktok, and all. |
| `mediaUrls[]` | body | `array<string>` | no | HTTPS image or video URLs to attach to the post. |
| `scheduleDate` | body | `date` | no | UTC ISO 8601 date and time to schedule the post. |
| `randomPost` | body | `boolean` | no | Generate random post text for testing instead of using Post Text. |
