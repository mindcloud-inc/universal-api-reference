# Readwise: Get Daily Review

Retrieves the daily review from Readwise.

```
GET https://connect.mindcloud.co/v1/universal/readwise/latest/actions/get-daily-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Readwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/get-daily-review?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/readwise/latest/actions/get-daily-review?${params}`, {
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
      "highlights": [
        {}
      ],
      "id": "string",
      "reviewId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `highlights[]` | object |  |
| `id` | string |  |
| `reviewId` | string |  |

## Native endpoint

Through the native Readwise API, this operation is `GET /api/v2/review/` (base URL `https://readwise.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-daily-review.md) for the provider-specific parameters and requirements.

