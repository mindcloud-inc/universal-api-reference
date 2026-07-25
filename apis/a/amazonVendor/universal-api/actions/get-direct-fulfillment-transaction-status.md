# Amazon Vendor: Get Direct Fulfillment Transaction Status



```
GET https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/get-direct-fulfillment-transaction-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Vendor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/get-direct-fulfillment-transaction-status?connectionId=$CONNECTION_ID&transactionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/get-direct-fulfillment-transaction-status?${params}`, {
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
| `transactionId` | string | yes | Transaction identifier returned from a Direct Fulfillment POST request. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amazon Vendor API returns.

## Native endpoint

Through the native Amazon Vendor API, this operation is `GET /vendor/directFulfillment/transactions/2021-12-28/transactions/:transactionId` (base URL `https://sellingpartnerapi-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-direct-fulfillment-transaction-status.md) for the provider-specific parameters and requirements.

