# Jobber: List Payments



```
GET https://connect.mindcloud.co/v1/universal/jobber/latest/actions/list-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jobber `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jobber/latest/actions/list-payments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jobber/latest/actions/list-payments?${params}`, {
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
| `columns` | string | no | Select the Jobber payment record fields to return. Default: `["id","adjustmentType","amount","entryDate","jobberPaymentLast4","jobberPaymentPaymentMethod","jobberPaymentTransactionStatus","tipAmount","allocations.nodes.invoice.id"]`. |
| `adjustmentType` | list | no | Only return payment records with the specified Jobber income adjustment type. One of: `BAD_DEBT`, `CORRECTION`, `DEPOSIT`, `FAILED_ACH_PAYMENT`, `INITIAL_BALANCE`, `INVOICE`, `PAYMENT`, `REFUND`, `VOIDED`. |
| `entryDateAfter` | date | no | Only return payment records created after this entry date (ISO 8601). Example: `2026-04-01T00:00:00.000Z`. |
| `entryDateBefore` | date | no | Only return payment records created before this entry date (ISO 8601). Example: `2026-05-01T00:00:00.000Z`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Jobber API returns.

## Native endpoint

Through the native Jobber API, this operation is `POST graphql` (base URL `https://api.getjobber.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payments.md) for the provider-specific parameters and requirements.

