# Wikipedia: Parse Page

Parses a Wikipedia page into HTML content.

```
GET https://connect.mindcloud.co/v1/universal/wikipedia/latest/actions/parse-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wikipedia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wikipedia/latest/actions/parse-page?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wikipedia/latest/actions/parse-page?${params}`, {
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
      "parse": {},
      "warnings": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `parse` | object | Parsed Wikipedia page output including rendered HTML and related metadata. |
| `warnings` | object | Parser warnings returned by the API. |

## Native endpoint

Through the native Wikipedia API, this operation is `GET /w/api.php?action=parse&prop=text|categories|links&format=json` (base URL `https://en.wikipedia.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-page.md) for the provider-specific parameters and requirements.

