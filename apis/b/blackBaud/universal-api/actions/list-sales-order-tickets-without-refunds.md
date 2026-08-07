# BlackBaud: List Sales Order Tickets Without Refunds



```
GET https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/list-sales-order-tickets-without-refunds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlackBaud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/list-sales-order-tickets-without-refunds?connectionId=$CONNECTION_ID&salesOrderId=Sales%20order%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "salesOrderId": "Sales order ID"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/list-sales-order-tickets-without-refunds?${params}`, {
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
| `salesOrderId` | string | yes | The Blackbaud sales order identifier. Example: `Sales order ID`. |
| `limit` | number | no | Maximum number of rows to return. Example: `100`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionKey` | string | no | Paging session key returned by Blackbaud for multi-page reads. |
| `infinitySession` | string | no | Blackbaud Infinity session identifier when required by the endpoint. |
| `moreRowsRangeKey` | string | no | Blackbaud cursor-like range key for additional rows. |
| `startRowIndex` | number | no | Row index to start returning results from. Example: `0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BlackBaud API returns.

## Native endpoint

Through the native BlackBaud API, this operation is `GET alt-slsmg/sales/{sales_order_id}/tickets` (base URL `https://api.sky.blackbaud.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sales-order-tickets-without-refunds.md) for the provider-specific parameters and requirements.

