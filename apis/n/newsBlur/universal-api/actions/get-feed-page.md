# NewsBlur: Get Feed Page

Retrieves a feed page from NewsBlur.

```
GET https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-feed-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-feed-page?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/get-feed-page?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Feed ID for the original page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "html": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html` | string | Feed page HTML returned by NewsBlur. |

## Native endpoint

Through the native NewsBlur API, this operation is `GET /reader/page/:id` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feed-page.md) for the provider-specific parameters and requirements.

