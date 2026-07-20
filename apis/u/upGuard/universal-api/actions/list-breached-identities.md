# UpGuard: List Breached Identities

Retrieves breached identities from your UpGuard account.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-breached-identities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-breached-identities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-breached-identities?${params}`, {
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
| `breachId` | string | no | The breach ID to filter on |
| `pageToken` | string | no | The page_token from a previous request, use this to get the next page of results. |
| `pageSize` | number | no | The number of results to return per page. Default: `1000`. |
| `sortBy` | string | no | The value to sort the breached identities by. |
| `sortDesc` | boolean | no | Whether or not to sort the results in descending order. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UpGuard API returns.

## Native endpoint

Through the native UpGuard API, this operation is `GET /breaches` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-breached-identities.md) for the provider-specific parameters and requirements.

