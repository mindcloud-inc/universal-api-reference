# Teachlr Organizations: List Draft Courses



```
GET https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/list-draft-courses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teachlr Organizations `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/list-draft-courses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/list-draft-courses?${params}`, {
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
| `search` | string | no | Word or phrase to match against course title, headline, or description. |
| `sort` | string | no | Course attribute to sort by, such as created_at or title. |
| `ord` | string | no | Sort direction: asc or desc. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cover": {},
      "created_at": "string",
      "description": "string",
      "expired": true,
      "headline": "string",
      "id": 1,
      "in_home": true,
      "is_public": true,
      "language": "string",
      "slug": "string",
      "status": "string",
      "title": "string",
      "url": "https://example.com",
      "views": 1,
      "visits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cover` | object |  |
| `created_at` | string |  |
| `description` | string |  |
| `expired` | boolean |  |
| `headline` | string |  |
| `id` | number |  |
| `in_home` | boolean |  |
| `is_public` | boolean |  |
| `language` | string |  |
| `slug` | string |  |
| `status` | string |  |
| `title` | string |  |
| `url` | string |  |
| `views` | number |  |
| `visits` | number |  |

## Native endpoint

Through the native Teachlr Organizations API, this operation is `GET /courses/draft` (base URL `https://api.teachlr.com/mindcloudteachlr337933/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-draft-courses.md) for the provider-specific parameters and requirements.

