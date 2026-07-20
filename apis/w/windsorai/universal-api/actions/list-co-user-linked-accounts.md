# Windsor.ai: List Co-User Linked Accounts

Retrieves co-user linked accounts from Windsor.ai.

```
GET https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/list-co-user-linked-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Windsor.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/list-co-user-linked-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/windsorai/latest/actions/list-co-user-linked-accounts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Windsor.ai API returns.

## Native endpoint

Through the native Windsor.ai API, this operation is `GET /api/team/co-user-linked-accounts/` (base URL `https://onboard.windsor.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-co-user-linked-accounts.md) for the provider-specific parameters and requirements.

