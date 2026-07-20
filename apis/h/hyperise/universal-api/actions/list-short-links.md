# Hyperise: List Short Links

Retrieves short links from Hyperise.

```
GET https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/list-short-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/list-short-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/list-short-links?${params}`, {
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
      "data": [
        {
          "createdAt": "string",
          "desc": "string",
          "id": 1,
          "link": "https://example.com",
          "linkHash": "https://example.com",
          "title": "string",
          "updatedAt": "string",
          "url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].createdAt` | string |  |
| `data[].desc` | string |  |
| `data[].id` | number |  |
| `data[].link` | string |  |
| `data[].linkHash` | string |  |
| `data[].title` | string |  |
| `data[].updatedAt` | string |  |
| `data[].url` | string |  |

## Native endpoint

Through the native Hyperise API, this operation is `GET /short-links` (base URL `https://app.hyperise.io/api/v1/regular`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-short-links.md) for the provider-specific parameters and requirements.

