# WebCategorize: List URL Tags



```
GET https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/list-url-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebCategorize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/list-url-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/list-url-tags?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | URL tag value. |

## Native endpoint

Through the native WebCategorize API, this operation is `GET /url/get/tags` (base URL `https://app.webcategorize.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-url-tags.md) for the provider-specific parameters and requirements.

