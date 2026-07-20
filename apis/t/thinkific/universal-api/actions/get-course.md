# Thinkific: Get Course

Retrieves a course record from Thinkific.

```
GET https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/get-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Thinkific `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/get-course?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/get-course?${params}`, {
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
| `id` | number | yes | Course identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "administratorUserIds": [
        1
      ],
      "chapterIds": [
        1
      ],
      "description": "string",
      "id": 1,
      "instructorId": 1,
      "name": "Ava Chen",
      "productId": 1,
      "reviewsEnabled": true,
      "slug": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administratorUserIds` | array<number> |  |
| `chapterIds` | array<number> |  |
| `description` | string |  |
| `id` | number |  |
| `instructorId` | number |  |
| `name` | string |  |
| `productId` | number |  |
| `reviewsEnabled` | boolean |  |
| `slug` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Thinkific API, this operation is `GET /courses/:id` (base URL `https://api.thinkific.com/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-course.md) for the provider-specific parameters and requirements.

