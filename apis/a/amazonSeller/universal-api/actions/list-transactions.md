# Amazon Seller: List Transactions

Retrieves finance transactions from Amazon Seller.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/list-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/list-transactions?${params}`, {
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
| `postedAfter` | date | no | Include transactions posted on or after this ISO 8601 date-time. This must be more than two minutes before the request time. |
| `postedBefore` | date | no | Include transactions posted before this ISO 8601 date-time. It must be later than Posted After and defaults to two minutes before the request time. |
| `marketplaceId` | string | no | Filter transactions to a specific marketplace ID. |
| `transactionStatus` | string | no | Filter by transaction status: DEFERRED, RELEASED, or DEFERRED_RELEASED. |
| `relatedIdentifierName` | string | no | Filter by identifier type: FINANCIAL_EVENT_GROUP_ID or ORDER_ID. |
| `relatedIdentifierValue` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amazon Seller API returns.

## Native endpoint

Through the native Amazon Seller API, this operation is `GET finances/2024-06-19/transactions` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

