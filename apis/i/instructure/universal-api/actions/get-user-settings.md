# Instructure: Get User Settings

Retrieves user settings from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-user-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-user-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-user-settings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Instructure API, this operation is `GET /users/self/settings` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-settings.md) for the provider-specific parameters and requirements.

