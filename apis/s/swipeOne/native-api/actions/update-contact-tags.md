# Update Contact Tags with Swipe One

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:contactId/tags`
- **Base URL:** `https://api.swipeone.com/api`
- **Official documentation:** [Update Contact Tags](https://docs.swipeone.com/en/articles/10545829-tags#h_9840d2c2ef)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contactId` | path | `string` | yes |
| `tags[]` | body | `array<string>` | no |
