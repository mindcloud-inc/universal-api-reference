# SMSup: Delete Subaccount



```
DELETE https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/delete-subaccount
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/delete-subaccount?connectionId=$CONNECTION_ID&userName=subaccount_user_name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userName": "subaccount_user_name"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/delete-subaccount?${params}`, {
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
| `userName` | string | yes | Username of the subaccount. Example: `subaccount_user_name`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMSup API returns.

## Native endpoint

Through the native SMSup API, this operation is `POST /api/3.0/subaccount/delete` (base URL `https://api.gateway360.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-subaccount.md) for the provider-specific parameters and requirements.

