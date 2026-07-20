# Codeberg: Get Current User Settings



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-current-user-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-current-user-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-current-user-settings?${params}`, {
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
      "description": "string",
      "diff_view_style": "string",
      "enable_repo_unit_hints": true,
      "full_name": "Ava Chen",
      "hide_activity": true,
      "hide_email": true,
      "hide_pronouns": true,
      "language": "string",
      "location": "string",
      "pronouns": "string",
      "theme": "string",
      "website": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `diff_view_style` | string |  |
| `enable_repo_unit_hints` | boolean |  |
| `full_name` | string |  |
| `hide_activity` | boolean |  |
| `hide_email` | boolean |  |
| `hide_pronouns` | boolean |  |
| `language` | string |  |
| `location` | string |  |
| `pronouns` | string |  |
| `theme` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /user/settings` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user-settings.md) for the provider-specific parameters and requirements.

