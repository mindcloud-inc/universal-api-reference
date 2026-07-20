# Teachlr Organizations: List Courses With Active Coupons



```
GET https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/list-courses-with-active-coupons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teachlr Organizations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/list-courses-with-active-coupons?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/list-courses-with-active-coupons?${params}`, {
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
      "expired": true,
      "hasCoupons": true,
      "headline": "string",
      "id": 1,
      "language": "string",
      "price": "string",
      "slug": "string",
      "status": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expired` | boolean |  |
| `hasCoupons` | boolean |  |
| `headline` | string |  |
| `id` | number |  |
| `language` | string |  |
| `price` | string |  |
| `slug` | string |  |
| `status` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Teachlr Organizations API, this operation is `GET /courses/available` (base URL `https://api.teachlr.com/mindcloudteachlr337933/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-courses-with-active-coupons.md) for the provider-specific parameters and requirements.

