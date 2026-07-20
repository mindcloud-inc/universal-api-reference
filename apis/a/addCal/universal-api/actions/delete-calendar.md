# AddCal: Delete Calendar

Deletes an existing calendar from AddCal.

```
DELETE https://connect.mindcloud.co/v1/universal/addCal/latest/actions/delete-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AddCal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/addCal/latest/actions/delete-calendar?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addCal/latest/actions/delete-calendar?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AddCal API returns.

## Native endpoint

Through the native AddCal API, this operation is `DELETE /calendars/:public_id` (base URL `https://addcal.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-calendar.md) for the provider-specific parameters and requirements.

