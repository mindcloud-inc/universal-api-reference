# Create Newsletter with Ghost

Creates a new newsletter in Ghost.

## Endpoint

- **Method:** `POST`
- **Path:** `/newsletters/`
- **Base URL:** `{adminDomain}/ghost/api/admin`
- **Official documentation:** [Create Newsletter](https://docs.ghost.org/admin-api/newsletters/creating-a-newsletter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opt_in_existing` | query | `boolean` | no | Whether existing members should be opted into the new newsletter. |
| `newsletters[0].name` | body | `string` | yes | Public name for the newsletter. |
| `newsletters[0].description` | body | `string` | no | Public description for the newsletter. |
| `newsletters[0].sender_reply_to` | body | `string` | no | Reply-to behavior for newsletter emails. |
| `newsletters[0].status` | body | `string` | no | Newsletter status. |
| `newsletters[0].subscribe_on_signup` | body | `boolean` | no | Whether new members should be subscribed on signup. |
| `newsletters[0].show_header_name` | body | `boolean` | no | Whether to show the site name in the newsletter header. |
| `newsletters[0].title_font_category` | body | `string` | no | Title font category, such as sans_serif. |
| `newsletters[0].title_alignment` | body | `string` | no | Title alignment, such as center. |
| `newsletters[0].show_badge` | body | `boolean` | no | Whether to show the newsletter badge. |
