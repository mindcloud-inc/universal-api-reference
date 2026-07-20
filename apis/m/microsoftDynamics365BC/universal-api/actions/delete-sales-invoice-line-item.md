# Microsoft Dynamics 365 BC: Delete Sales Invoice Line Item



```
DELETE https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/delete-sales-invoice-line-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 BC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/delete-sales-invoice-line-item?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/delete-sales-invoice-line-item?${params}`, {
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
| `companyId` | list<string> | no | The Id of the company. This Id can be find on the "Get Companies" Action |
| `salesInvoiceId` | string | no |  |
| `lineItemId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 BC API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 BC API, this operation is `DELETE v2.0/companies(:companyId)/salesInvoices(:salesInvoiceId)/salesInvoiceLines(:lineItemId)` (base URL `https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-sales-invoice-line-item.md) for the provider-specific parameters and requirements.

