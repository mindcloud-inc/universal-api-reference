# Rillion Prime Web Service: List Invoices Missing Payment Date

List invoices that have no payment date registered in Prime.

```
GET https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-invoices-missing-payment-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-invoices-missing-payment-date?connectionId=$CONNECTION_ID&fromAccountCodingDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromAccountCodingDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-invoices-missing-payment-date?${params}`, {
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
| `company` | list<string> | no | Company ID to scope the call. |
| `fromAccountCodingDate` | string | yes | Only include invoices with accounting date on or after this date (yyyy-MM-dd). The server rejects the call without it (verified live). |
| `erpFilter` | string | no | ERP identifier to filter by. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoices-missing-payment-date.md) for the provider-specific parameters and requirements.

