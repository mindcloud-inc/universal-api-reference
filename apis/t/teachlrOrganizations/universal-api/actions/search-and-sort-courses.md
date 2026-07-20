# Teachlr Organizations: Search And Sort Courses



```
GET https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/search-and-sort-courses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teachlr Organizations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/search-and-sort-courses?connectionId=$CONNECTION_ID&search=plan&sort=title" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "search": "plan",
  "sort": "title"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/search-and-sort-courses?${params}`, {
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
| `search` | string | yes | Word or phrase to search in course title, subtitle, or description. Default: `plan`. |
| `sort` | string | yes | Course field to sort by. Default: `title`. |
| `ord` | string | no | Sort direction. Default: `desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expired": true,
      "headline": "string",
      "id": 1,
      "language": "string",
      "numSales": 1,
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
| `headline` | string |  |
| `id` | number |  |
| `language` | string |  |
| `numSales` | number |  |
| `price` | string |  |
| `slug` | string |  |
| `status` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Teachlr Organizations API, this operation is `GET /courses/available` (base URL `https://api.teachlr.com/mindcloudteachlr337933/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-and-sort-courses.md) for the provider-specific parameters and requirements.

