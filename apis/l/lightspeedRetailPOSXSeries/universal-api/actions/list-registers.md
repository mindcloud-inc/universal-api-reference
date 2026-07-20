# Lightspeed Retail POS (X-Series): List Registers

Retrieves registers from Lightspeed Retail POS (X-Series).

```
GET https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/list-registers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightspeed Retail POS (X-Series) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/list-registers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightspeedRetailPOSXSeries/latest/actions/list-registers?${params}`, {
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
      "askForNoteOnSave": "string",
      "askForUserOnSale": "string",
      "attributes": "string",
      "buttonLayoutId": "string",
      "cashManagedPaymentTypeId": "string",
      "deletedAt": "string",
      "emailReceipt": "ava@example.com",
      "id": "string",
      "invoicePrefix": "string",
      "invoiceSequence": "string",
      "invoiceSuffix": "string",
      "isOpen": "string",
      "isQuickKeysEnabled": "string",
      "name": "Ava Chen",
      "outletId": "string",
      "printNoteOnReceipt": "string",
      "printReceipt": "string",
      "receiptTemplateId": "string",
      "registerCloseTime": "string",
      "registerOpenSequenceId": "string",
      "registerOpenTime": "string",
      "showDiscountsOnReceipts": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `askForNoteOnSave` | string |  |
| `askForUserOnSale` | string |  |
| `attributes` | string |  |
| `buttonLayoutId` | string |  |
| `cashManagedPaymentTypeId` | string |  |
| `deletedAt` | string |  |
| `emailReceipt` | string |  |
| `id` | string |  |
| `invoicePrefix` | string |  |
| `invoiceSequence` | string |  |
| `invoiceSuffix` | string |  |
| `isOpen` | string |  |
| `isQuickKeysEnabled` | string |  |
| `name` | string |  |
| `outletId` | string |  |
| `printNoteOnReceipt` | string |  |
| `printReceipt` | string |  |
| `receiptTemplateId` | string |  |
| `registerCloseTime` | string |  |
| `registerOpenSequenceId` | string |  |
| `registerOpenTime` | string |  |
| `showDiscountsOnReceipts` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Lightspeed Retail POS (X-Series) API, this operation is `GET /api/2.0/registers` (base URL `https://{{credentials.authorizeRequest.domain_prefix}}.retail.lightspeed.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-registers.md) for the provider-specific parameters and requirements.

