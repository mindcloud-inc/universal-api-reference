# Validate Post with Ayrshare

Validates a post before publishing in Ayrshare.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/post`
- **Base URL:** `https://api.ayrshare.com/api`
- **Official documentation:** [Validate Post](https://www.ayrshare.com/docs/apis/validate/validate-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `post` | body | `string` | yes | Post text to validate before publishing. |
| `platforms[]` | body | `array<string>` | yes | Platforms to validate the post against. |
