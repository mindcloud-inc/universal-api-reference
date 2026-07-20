# Eventee: List Reviews

Retrieves reviews from Eventee.

```
GET https://connect.mindcloud.co/v1/universal/eventee/latest/actions/list-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventee/latest/actions/list-reviews?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventee/latest/actions/list-reviews?${params}`, {
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
      "comment": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "device": "string",
      "id": 1,
      "lecture": {},
      "lectureId": 1,
      "OS": "string",
      "stars": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1,
      "username": "Ava Chen",
      "userphoto": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string | Review comment text. |
| `createdAt` | date | Review creation datetime. |
| `device` | string | Client device label. |
| `id` | number | Review ID. |
| `lecture` | object | Lecture object tied to the review. |
| `lectureId` | number | Reviewed lecture ID. |
| `OS` | string | Client operating system. |
| `stars` | number | Star rating. |
| `updatedAt` | date | Review update datetime. |
| `userId` | number | Reviewer user ID. |
| `username` | string | Reviewer username. |
| `userphoto` | string | Reviewer photo URL. |

## Native endpoint

Through the native Eventee API, this operation is `GET /reviews` (base URL `https://api.eventee.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reviews.md) for the provider-specific parameters and requirements.

