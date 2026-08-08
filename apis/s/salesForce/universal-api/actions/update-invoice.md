# Salesforce: Update Order Items



```
PUT https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesForce/latest/actions/update-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no |  |
| `vendorInvoiceNumber` | string | no |  |
| `carrier` | string | no |  |
| `trackingNumber` | string | no |  |
| `serviceType` | string | no |  |
| `productStatus` | string | no |  |
| `Synced__c` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "reauthenticationResponse": {
        "details": "string"
      },
      "response": {
        "code": "string",
        "data": [
          {
            "errorCode": "string",
            "message": "string"
          }
        ],
        "message": "string",
        "name": "Ava Chen",
        "stack": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reauthenticationResponse.details` | string |  |
| `response.code` | string |  |
| `response.data[].errorCode` | string |  |
| `response.data[].message` | string |  |
| `response.message` | string |  |
| `response.name` | string |  |
| `response.stack` | string |  |

## Native endpoint

Through the native Salesforce API, this operation is `PATCH services/data/v61.0/sobjects/OrderItem/:id` (base URL `https://{{credentials.companyDomainName}}.my.salesforce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.

