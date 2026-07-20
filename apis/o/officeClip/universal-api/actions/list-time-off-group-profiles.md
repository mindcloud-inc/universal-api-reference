# OfficeClip: List Time Off Group Profiles

Retrieves time off group profiles from OfficeClip.

```
GET https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-time-off-group-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeClip `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-time-off-group-profiles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-time-off-group-profiles?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OfficeClip API returns.

## Native endpoint

Through the native OfficeClip API, this operation is `GET /api/timeoff-group-profile` (base URL `https://app.officeclip.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-time-off-group-profiles.md) for the provider-specific parameters and requirements.

