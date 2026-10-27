# Viewpoint Vista: Search AP Objects

Search objects found in the Viewpoint® Vista™ Accounts Payable (AP) programs.

```
GET https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/search-ap-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/search-ap-objects?connectionId=$CONNECTION_ID&object=company_parameters" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "object": "company_parameters"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/search-ap-objects?${params}`, {
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
| `modifiedUtcAfter` | date | no | Specify a datetime against which to filter the results. |
| `modifiedUtcBefore` | date | no | Specify a datetime against which to filter the results. |
| `object` | list<string> | yes | Specify the type of Object from the Accounts Payable V2 Direct API that you'd like to retrieve. One of: `company_parameters`, `inv_batch_entries`, `inv_batches`, `invoice_holds`, `invoice_line_details`, `invoices`, `pay_batch_entries`, `pay_batches`, `pay_categories`, `pay_types`, `payment_histories`, `rel_ret_bat_entries`, `rel_retainage_batch`, `unapproved_invoices`, `vendor_compliances`, `vendor_holds`, `vendors`. |
| `filters[]` | array<object> | no |  |
| `filters` | object | no |  |
| `filters[].operator` | string | no |  |
| `filters[].propertyName` | string | no |  |
| `filters[].value` | string | no |  |
| `filters[].numberValue` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-ap-objects.md) for the provider-specific parameters and requirements.

