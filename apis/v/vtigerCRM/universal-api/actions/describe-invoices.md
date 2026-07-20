# Vtiger CRM: Describe Invoices

Retrieves invoice metadata from Vtiger CRM.

```
GET https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/describe-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vtiger CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/describe-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/describe-invoices?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createable": true,
      "deleteable": true,
      "idPrefix": "string",
      "isEntity": true,
      "label": "string",
      "name": "Ava Chen",
      "retrieveable": true,
      "updateable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createable` | boolean | Whether records can be created. |
| `deleteable` | boolean | Whether records can be deleted. |
| `idPrefix` | string | Vtiger id prefix for records in this module. |
| `isEntity` | boolean | Whether the module is a standard entity module. |
| `label` | string | Module label. |
| `name` | string | Module API name. |
| `retrieveable` | boolean | Whether records can be retrieved. |
| `updateable` | boolean | Whether records can be updated. |

## Native endpoint

Through the native Vtiger CRM API, this operation is `GET /describe?elementType=Invoice` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/describe-invoices.md) for the provider-specific parameters and requirements.

