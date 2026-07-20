# Codeberg: Get UI Settings



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-ui-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-ui-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-ui-settings?${params}`, {
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
      "allowed_reactions": [
        "string"
      ],
      "custom_emojis": [
        "string"
      ],
      "default_theme": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowed_reactions` | array<string> |  |
| `custom_emojis` | array<string> |  |
| `default_theme` | string |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /settings/ui` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ui-settings.md) for the provider-specific parameters and requirements.

