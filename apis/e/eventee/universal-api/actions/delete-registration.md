# Eventee: Delete Registration

Deletes a registration from Eventee.

```
DELETE https://connect.mindcloud.co/v1/universal/eventee/latest/actions/delete-registration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eventee/latest/actions/delete-registration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventee/latest/actions/delete-registration?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Eventee API returns.

## Native endpoint

Through the native Eventee API, this operation is `DELETE /registration` (base URL `https://api.eventee.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-registration.md) for the provider-specific parameters and requirements.

