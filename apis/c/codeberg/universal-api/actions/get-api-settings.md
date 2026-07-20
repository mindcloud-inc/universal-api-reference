# Codeberg: Get API Settings



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-api-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-api-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/get-api-settings?${params}`, {
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
      "default_git_trees_per_page": 1,
      "default_max_blob_size": 1,
      "default_paging_num": 1,
      "max_response_items": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default_git_trees_per_page` | number |  |
| `default_max_blob_size` | number |  |
| `default_paging_num` | number |  |
| `max_response_items` | number |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /settings/api` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-settings.md) for the provider-specific parameters and requirements.

