# Cloutly: List Businesses

Retrieves businesses connected to your Cloutly account.

```
GET https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/list-businesses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloutly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/list-businesses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/list-businesses?${params}`, {
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
      "coverPhotoUrl": "https://example.com",
      "id": "string",
      "logoSrc": "string",
      "name": "Ava Chen",
      "rating": "string",
      "sourceMap": [
        "string"
      ],
      "sources": [
        "string"
      ],
      "totalReviews": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `coverPhotoUrl` | string |  |
| `id` | string |  |
| `logoSrc` | string |  |
| `name` | string |  |
| `rating` | string |  |
| `sourceMap` | array |  |
| `sources` | array |  |
| `totalReviews` | number |  |

## Native endpoint

Through the native Cloutly API, this operation is `GET /businesses` (base URL `https://app.cloutly.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-businesses.md) for the provider-specific parameters and requirements.

