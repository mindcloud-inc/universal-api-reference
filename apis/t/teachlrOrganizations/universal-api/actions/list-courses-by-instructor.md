# Teachlr Organizations: List Courses By Instructor



```
GET https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/list-courses-by-instructor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teachlr Organizations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/list-courses-by-instructor?connectionId=$CONNECTION_ID&instructor=pedroperez" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "instructor": "pedroperez"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/list-courses-by-instructor?${params}`, {
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
| `instructor` | string | yes | Username of the instructor whose courses should be listed. Default: `pedroperez`. |

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

Through the native Teachlr Organizations API, this operation is `GET /courses/available` (base URL `https://api.teachlr.com/mindcloudteachlr337933/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-courses-by-instructor.md) for the provider-specific parameters and requirements.

