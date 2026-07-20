# OnlineCheckWriter: Get ACH Withdrawal

Retrieves the status and details of a specific ACH withdrawal.

```
GET https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-ach-withdrawal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnlineCheckWriter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-ach-withdrawal?connectionId=$CONNECTION_ID&withdrawalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "withdrawalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-ach-withdrawal?${params}`, {
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
| `withdrawalId` | string | yes | The withdrawal identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OnlineCheckWriter API returns.

## Native endpoint

Through the native OnlineCheckWriter API, this operation is `GET /wallet/withdraw/ach/:withdrawalId` (base URL `https://test.onlinecheckwriter.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ach-withdrawal.md) for the provider-specific parameters and requirements.

