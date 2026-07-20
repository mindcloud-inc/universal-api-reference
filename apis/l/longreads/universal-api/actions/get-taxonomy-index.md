# Longreads: Get Taxonomy Index

Retrieves taxonomy definitions from the Longreads site.

```
GET https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-taxonomy-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Longreads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-taxonomy-index?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-taxonomy-index?${params}`, {
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
      "description": "string",
      "name": "Ava Chen",
      "rest_base": "string",
      "slug": "string",
      "types": [
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
| `description` | string |  |
| `name` | string |  |
| `rest_base` | string |  |
| `slug` | string |  |
| `types` | array<string> |  |

## Native endpoint

Through the native Longreads API, this operation is `GET /wp/v2/taxonomies` (base URL `https://longreads.com/wp-json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-taxonomy-index.md) for the provider-specific parameters and requirements.

