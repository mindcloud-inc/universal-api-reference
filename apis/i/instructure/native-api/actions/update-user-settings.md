# Update User Settings with Instructure

Updates user settings in Instructure Canvas.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/self/settings`
- **Base URL:** `https://canvas.instructure.com/api/v1`
- **Official documentation:** [Update User Settings](https://developerdocs.instructure.com/services/canvas/resources/users#method.users.settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collapse_course_nav` | body | `boolean` | no | Whether to collapse the course navigation. |
| `collapse_global_nav` | body | `boolean` | no | Whether to collapse the global navigation. |
| `comment_library_suggestions_enabled` | body | `boolean` | no | Whether comment library suggestions are enabled. |
| `default_to_block_editor` | body | `boolean` | no | Whether to default to the block editor. |
| `elementary_dashboard_disabled` | body | `boolean` | no | Whether the elementary dashboard is disabled. |
| `hide_dashcard_color_overlays` | body | `boolean` | no | Whether to hide dashcard color overlays. |
| `release_notes_badge_disabled` | body | `boolean` | no | Whether the release notes badge is disabled. |
| `widget_dashboard_dark_mode` | body | `boolean` | no | Widget dashboard dark mode toggle. |
| `widget_dashboard_user_preference` | body | `boolean` | no | Widget dashboard user preference toggle. |
