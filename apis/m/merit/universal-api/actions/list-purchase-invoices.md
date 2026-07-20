# Merit: List Purchase Invoices



```
GET https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-purchase-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-purchase-invoices?connectionId=$CONNECTION_ID&periodStart=20260401&periodEnd=20260430&dateType=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "periodStart": "20260401",
  "periodEnd": "20260430",
  "dateType": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merit/latest/actions/list-purchase-invoices?${params}`, {
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
| `periodStart` | string | yes | Start date in YYYYmmDD format. Example: `20260401`. |
| `periodEnd` | string | yes | End date in YYYYmmDD format. Example: `20260430`. |
| `unPaid` | boolean | no | Whether to return only unpaid documents. |
| `dateType` | number | yes | 0 for document date, 1 for changed date. Example: `0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Merit API returns.

## Native endpoint

Through the native Merit API, this operation is `POST v2/getpurchorders` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-purchase-invoices.md) for the provider-specific parameters and requirements.

