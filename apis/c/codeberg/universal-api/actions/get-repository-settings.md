# Codeberg: Get Repository Settings



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-repository-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-repository-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-repository-settings?${params}`, {
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
      "forks_disabled": true,
      "http_git_disabled": true,
      "lfs_disabled": true,
      "migrations_disabled": true,
      "mirrors_disabled": true,
      "stars_disabled": true,
      "time_tracking_disabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `forks_disabled` | boolean |  |
| `http_git_disabled` | boolean |  |
| `lfs_disabled` | boolean |  |
| `migrations_disabled` | boolean |  |
| `mirrors_disabled` | boolean |  |
| `stars_disabled` | boolean |  |
| `time_tracking_disabled` | boolean |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /settings/repository` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-repository-settings.md) for the provider-specific parameters and requirements.

