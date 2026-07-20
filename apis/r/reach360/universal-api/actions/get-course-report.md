# Reach360: Get Course Report

Retrieves a course report from Reach360.

```
GET https://connect.mindcloud.co/v1/universal/reach360/latest/actions/get-course-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reach360 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reach360/latest/actions/get-course-report?connectionId=$CONNECTION_ID&limit=25&offset=0&courseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "courseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reach360/latest/actions/get-course-report?${params}`, {
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
| `courseId` | string | yes | The course ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Reach360 API returns.

## Native endpoint

Through the native Reach360 API, this operation is `GET /reports/courses/:courseId` (base URL `https://api.reach360.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-course-report.md) for the provider-specific parameters and requirements.

