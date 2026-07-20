# Bulk24SMS: View Own Profile

Retrieves your user profile from Bulk24SMS.

```
GET https://connect.mindcloud.co/v1/universal/bulk24SMS/latest/actions/view-own-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulk24SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulk24SMS/latest/actions/view-own-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulk24SMS/latest/actions/view-own-profile?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bulk24SMS API returns.

## Native endpoint

Through the native Bulk24SMS API, this operation is `GET` (base URL `https://api.bulk24sms.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-own-profile.md) for the provider-specific parameters and requirements.

