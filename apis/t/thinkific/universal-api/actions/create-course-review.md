# Thinkific: Create Course Review

Creates a new course review in Thinkific.

```
POST https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/create-course-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Thinkific `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/create-course-review" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "approved": true,
  "courseId": 1,
  "rating": 1,
  "reviewText": "string",
  "title": "string",
  "userId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/create-course-review', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "approved": true,
    "courseId": 1,
    "rating": 1,
    "reviewText": "string",
    "title": "string",
    "userId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `approved` | boolean | yes | Whether the review is approved. |
| `courseId` | number | yes | Course ID for the review. |
| `rating` | number | yes | Review rating. |
| `reviewText` | string | yes | Review text content. |
| `title` | string | yes | Review title. |
| `userId` | number | yes | ID of the user creating the review. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approved": true,
      "courseId": 1,
      "createdAt": "string",
      "id": 1,
      "rating": 1,
      "reviewText": "string",
      "title": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approved` | boolean |  |
| `courseId` | number |  |
| `createdAt` | string |  |
| `id` | number |  |
| `rating` | number |  |
| `reviewText` | string |  |
| `title` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Thinkific API, this operation is `POST /course_reviews` (base URL `https://api.thinkific.com/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-course-review.md) for the provider-specific parameters and requirements.

