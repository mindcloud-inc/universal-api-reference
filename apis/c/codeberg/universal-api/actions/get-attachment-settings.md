# Codeberg: Get Attachment Settings



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-attachment-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-attachment-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-attachment-settings?${params}`, {
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
      "allowed_types": [
        "string"
      ],
      "enabled": true,
      "max_files": 1,
      "max_size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowed_types` | array<string> |  |
| `enabled` | boolean |  |
| `max_files` | number |  |
| `max_size` | number |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /settings/attachment` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attachment-settings.md) for the provider-specific parameters and requirements.

