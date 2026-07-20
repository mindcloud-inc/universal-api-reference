# Vouchsafe: List Alert Accounts

Retrieves monitored alert accounts from Vouchsafe.

```
GET https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/list-alert-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchsafe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/list-alert-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/list-alert-accounts?${params}`, {
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
| `status` | list | no | Filter monitored accounts by alert status. One of: `acknowledged`, `clear`, `new`. |
| `cursor` | string | no | Cursor for pagination using the ID of the last item from the previous page. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vouchsafe API returns.

## Native endpoint

Through the native Vouchsafe API, this operation is `GET /alerts/accounts` (base URL `https://app.vouchsafe.id/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alert-accounts.md) for the provider-specific parameters and requirements.

