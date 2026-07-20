# Scrapeless: List Browser Extensions

Retrieves browser extensions from Scrapeless.

```
GET https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/list-browser-extensions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/list-browser-extensions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/list-browser-extensions?${params}`, {
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
      "items": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[]` | array<object> |  |
| `items[].extensionId` | string | extension id |
| `items[].name` | string | extension name |
| `items[].version` | string | extension version |

## Native endpoint

Through the native Scrapeless API, this operation is `GET /browser/extensions/list` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-browser-extensions.md) for the provider-specific parameters and requirements.

