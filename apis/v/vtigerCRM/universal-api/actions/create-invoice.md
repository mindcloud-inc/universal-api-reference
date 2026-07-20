# Vtiger CRM: Create Invoice

Creates a new invoice in Vtiger CRM.

```
POST https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vtiger CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "element": {
    "qty1": "1",
    "subject": "Stage3 Default Invoice",
    "listPrice1": "10",
    "bill_street": "123 Billing St",
    "ship_street": "123 Shipping St",
    "productName1": "Stage3 Default Product Updated",
    "hdnProductId1": "6x509",
    "assigned_user_id": "19x1",
    "totalProductCount": "1"
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "element": {"qty1":"1","subject":"Stage3 Default Invoice","listPrice1":"10","bill_street":"123 Billing St","ship_street":"123 Shipping St","productName1":"Stage3 Default Product Updated","hdnProductId1":"6x509","assigned_user_id":"19x1","totalProductCount":"1"}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `element` | string | yes | JSON string for an Invoice payload. Include `subject`, `assigned_user_id`, `bill_street`, `ship_street`, and numbered line-item keys like `hdnProductId1`, `productName1`, `qty1`, `listPrice1`, `totalProductCount`. Default: `{"qty1":"1","subject":"Stage3 Default Invoice","listPrice1":"10","bill_street":"123 Billing St","ship_street":"123 Shipping St","productName1":"Stage3 Default Product Updated","hdnProductId1":"6x509","assigned_user_id":"19x1","totalProductCount":"1"}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "label": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Vtiger Invoice id. |
| `label` | string | Invoice label. |
| `url` | string | Invoice URL in Vtiger. |

## Native endpoint

Through the native Vtiger CRM API, this operation is `POST /create?elementType=Invoice` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice.md) for the provider-specific parameters and requirements.

