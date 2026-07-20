# Get User Dashboard with Tumblr

Retrieves the authenticated user's Tumblr dashboard.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/user/dashboard`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [Get User Dashboard](https://www.tumblr.com/docs/en/api/v2#userdashboard--retrieve-a-users-dashboard)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `list<string>` | no | Post type to return. Accepted values: `answer`, `audio`, `chat`, `link`, `photo`, `quote`, `text`, `video`. |
| `since_id` | query | `string` | no | Return posts that have appeared after this ID. |
| `reblog_info` | query | `boolean` | no | Return reblog information. |
| `notes_info` | query | `boolean` | no | Return note count and note metadata. |
