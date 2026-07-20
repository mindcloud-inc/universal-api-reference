# Teachlr Organizations: List Paginated Careers Without Embedded Courses



```
GET https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/list-paginated-careers-without-embedded-courses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teachlr Organizations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/list-paginated-careers-without-embedded-courses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/list-paginated-careers-without-embedded-courses?${params}`, {
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
| `page` | number | no | Page number to retrieve. Default: `1`. |
| `limit` | number | no | Number of careers per page. Default: `8`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasCoupons": true,
      "headline": "string",
      "id": 1,
      "language": "string",
      "numCourses": 1,
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
| `hasCoupons` | boolean |  |
| `headline` | string |  |
| `id` | number |  |
| `language` | string |  |
| `numCourses` | number |  |
| `price` | string |  |
| `slug` | string |  |
| `status` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Teachlr Organizations API, this operation is `GET /careers` (base URL `https://api.teachlr.com/mindcloudteachlr337933/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-paginated-careers-without-embedded-courses.md) for the provider-specific parameters and requirements.

