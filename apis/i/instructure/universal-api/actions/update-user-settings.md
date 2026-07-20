# Instructure: Update User Settings

Updates user settings in Instructure Canvas.

```
PUT https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-user-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-user-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/update-user-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collapseCourseNav` | boolean | no | Whether to collapse the course navigation. |
| `collapseGlobalNav` | boolean | no | Whether to collapse the global navigation. |
| `commentLibrarySuggestionsEnabled` | boolean | no | Whether comment library suggestions are enabled. |
| `defaultToBlockEditor` | boolean | no | Whether to default to the block editor. |
| `elementaryDashboardDisabled` | boolean | no | Whether the elementary dashboard is disabled. |
| `hideDashcardColorOverlays` | boolean | no | Whether to hide dashcard color overlays. |
| `releaseNotesBadgeDisabled` | boolean | no | Whether the release notes badge is disabled. |
| `widgetDashboardDarkMode` | boolean | no | Widget dashboard dark mode toggle. |
| `widgetDashboardUserPreference` | boolean | no | Widget dashboard user preference toggle. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collapse_course_nav": true,
      "collapse_global_nav": true,
      "comment_library_suggestions_enabled": true,
      "default_to_block_editor": true,
      "elementary_dashboard_disabled": true,
      "hide_dashcard_color_overlays": true,
      "manual_mark_as_read": true,
      "release_notes_badge_disabled": true,
      "widget_dashboard_dark_mode": true,
      "widget_dashboard_user_preference": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collapse_course_nav` | boolean |  |
| `collapse_global_nav` | boolean |  |
| `comment_library_suggestions_enabled` | boolean |  |
| `default_to_block_editor` | boolean |  |
| `elementary_dashboard_disabled` | boolean |  |
| `hide_dashcard_color_overlays` | boolean |  |
| `manual_mark_as_read` | boolean |  |
| `release_notes_badge_disabled` | boolean |  |
| `widget_dashboard_dark_mode` | boolean |  |
| `widget_dashboard_user_preference` | boolean |  |

## Native endpoint

Through the native Instructure API, this operation is `PUT /users/self/settings` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-settings.md) for the provider-specific parameters and requirements.

