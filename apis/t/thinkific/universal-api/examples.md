# Thinkific Universal API Examples

These examples use the MindCloud API key and Thinkific connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves user records from Thinkific.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/list-users?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/thinkific/latest/actions/list-users).

## Create Course Review

Creates a new course review in Thinkific.

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

Example response:

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

See the full [Create Course Review action reference](actions/create-course-review.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/thinkific/latest/actions/create-course-review).
