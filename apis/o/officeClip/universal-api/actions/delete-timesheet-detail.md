# OfficeClip: Delete Timesheet Detail

Deletes a timesheet detail from OfficeClip.

```
DELETE https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/delete-timesheet-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeClip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/delete-timesheet-detail?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/delete-timesheet-detail?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OfficeClip API returns.

## Native endpoint

Through the native OfficeClip API, this operation is `DELETE /api/timesheet-detail/{id}` (base URL `https://app.officeclip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-timesheet-detail.md) for the provider-specific parameters and requirements.

