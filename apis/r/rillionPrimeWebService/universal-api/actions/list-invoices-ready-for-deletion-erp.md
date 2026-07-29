# Rillion Prime Web Service: List Invoices Ready for Deletion ERP

List invoices marked ready for deletion for one ERP.

```
GET https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-invoices-ready-for-deletion-erp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-invoices-ready-for-deletion-erp?connectionId=$CONNECTION_ID&updateQueueStatus=false" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "updateQueueStatus": "false"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-invoices-ready-for-deletion-erp?${params}`, {
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
| `erp` | string | no | ERP identifier configured in Rillion Prime. |
| `updateQueueStatus` | boolean | yes | When true, returned rows are marked as exported and leave the queue permanently. Keep false to read without consuming. Default: `false`. |
| `company` | list<string> | no | Company ID to scope the call. |
| `noOfRows` | string | no | Maximum number of rows to return. Leave empty for no limit. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoices-ready-for-deletion-erp.md) for the provider-specific parameters and requirements.

