# OfficeClip: List TE Comments

Retrieves timesheet and expense comments from OfficeClip.

```
GET https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-te-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeClip `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-te-comments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-te-comments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OfficeClip API returns.

## Native endpoint

Through the native OfficeClip API, this operation is `GET /api/te-comments` (base URL `https://app.officeclip.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-te-comments.md) for the provider-specific parameters and requirements.

