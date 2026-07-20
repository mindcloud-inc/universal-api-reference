# Codeberg: List Current User Quota Attachments



```
GET https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-current-user-quota-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codeberg `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-current-user-quota-attachments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeberg/latest/actions/list-current-user-quota-attachments?${params}`, {
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
      "api_url": "https://example.com",
      "contained_in": {
        "api_url": "https://example.com",
        "html_url": "https://example.com"
      },
      "name": "Ava Chen",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_url` | string |  |
| `contained_in.api_url` | string |  |
| `contained_in.html_url` | string |  |
| `name` | string |  |
| `size` | number |  |

## Native endpoint

Through the native Codeberg API, this operation is `GET /user/quota/attachments` (base URL `https://codeberg.org/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-current-user-quota-attachments.md) for the provider-specific parameters and requirements.

