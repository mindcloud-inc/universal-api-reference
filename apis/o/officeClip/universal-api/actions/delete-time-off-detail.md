# OfficeClip: Delete Time Off Detail

Deletes a time off entry from OfficeClip.

```
DELETE https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/delete-time-off-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeClip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/delete-time-off-detail?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/delete-time-off-detail?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OfficeClip API returns.

## Native endpoint

Through the native OfficeClip API, this operation is `DELETE /api/timeoff-detail/{id}` (base URL `https://app.officeclip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-time-off-detail.md) for the provider-specific parameters and requirements.

