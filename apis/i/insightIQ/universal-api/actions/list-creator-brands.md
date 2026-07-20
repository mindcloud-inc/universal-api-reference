# InsightIQ: List Creator Brands

Retrieves available creator brands from InsightIQ.

```
GET https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/list-creator-brands
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InsightIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/list-creator-brands?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/list-creator-brands?${params}`, {
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
      "brands": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brands` | array<string> |  |

## Native endpoint

Through the native InsightIQ API, this operation is `GET /v1/social/creators/dictionary/brands` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-creator-brands.md) for the provider-specific parameters and requirements.

