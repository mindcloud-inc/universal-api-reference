# BILL Payables & Receivables: List Approvers Assigned to a Bill

Retrieves approvers assigned to a bill in Bill.com.

```
GET https://connect.mindcloud.co/v1/universal/billcom/latest/actions/list-bill-approvers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BILL Payables & Receivables `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billcom/latest/actions/list-bill-approvers?connectionId=$CONNECTION_ID&objectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "objectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billcom/latest/actions/list-bill-approvers?${params}`, {
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
| `objectId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BILL Payables & Receivables API returns.

## Native endpoint

Through the native BILL Payables & Receivables API, this operation is `POST ListApprovers.json` (base URL `https://api.bill.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bill-approvers.md) for the provider-specific parameters and requirements.

