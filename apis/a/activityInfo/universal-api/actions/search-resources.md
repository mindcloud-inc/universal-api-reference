# ActivityInfo: Search Resources

Finds resources in ActivityInfo by search query.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/search-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/search-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/search-resources?${params}`, {
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
      "partial": true,
      "results": [
        {}
      ],
      "searchString": "string",
      "truncated": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `partial` | boolean | Whether the response is partial. |
| `results` | array<object> | Matching resources. |
| `searchString` | string | Search string. |
| `truncated` | boolean | Whether results were truncated. |

## Native endpoint

Through the native ActivityInfo API, this operation is `GET /resources/search` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-resources.md) for the provider-specific parameters and requirements.

