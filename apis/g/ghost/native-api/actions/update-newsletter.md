# Update Newsletter with Ghost

Updates an existing newsletter in Ghost.

## Endpoint

- **Method:** `PUT`
- **Path:** `/newsletters/:id/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Update Newsletter](https://docs.ghost.org/admin-api/newsletters/updating-a-newsletter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Ghost newsletter ID from the URL path. |
| `newsletters[0].name` | body | `string` | no | Updated public name for the newsletter. |
| `newsletters[0].description` | body | `string` | no | Updated public description for the newsletter. |
| `newsletters[0].sender_name` | body | `string` | no | Updated sender name. |
| `newsletters[0].sender_email` | body | `string` | no | Updated sender email address. |
| `newsletters[0].sender_reply_to` | body | `string` | no | Updated reply-to behavior for newsletter emails. |
| `newsletters[0].status` | body | `string` | no | Updated newsletter status. |
| `newsletters[0].subscribe_on_signup` | body | `boolean` | no | Whether new members should be subscribed on signup. |
| `newsletters[0].sort_order` | body | `number` | no | Display order for the newsletter. |
| `newsletters[0].title_font_category` | body | `string` | no | Updated title font category. |
| `newsletters[0].title_alignment` | body | `string` | no | Updated title alignment. |
| `newsletters[0].show_badge` | body | `boolean` | no | Whether to show the newsletter badge. |
| `newsletters[0].show_header_name` | body | `boolean` | no | Whether to show the site name in the newsletter header. |
