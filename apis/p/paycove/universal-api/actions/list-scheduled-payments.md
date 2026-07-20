# Paycove: List Scheduled Payments

Retrieves scheduled payments from Paycove.

```
GET https://connect.mindcloud.co/v1/universal/paycove/latest/actions/list-scheduled-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/list-scheduled-payments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycove/latest/actions/list-scheduled-payments?${params}`, {
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
| `endDueDate` | date | no | Filter scheduled payments due on or before this date. |
| `startDueDate` | date | no | Filter scheduled payments due on or after this date. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Paycove API returns.

## Native endpoint

Through the native Paycove API, this operation is `GET scheduled-payments` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-scheduled-payments.md) for the provider-specific parameters and requirements.

