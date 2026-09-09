# Acumatica: Get Purchase Order



```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-purchase-order?connectionId=$CONNECTION_ID&id=f6f7701a-28c1-e411-9469-126b3844335e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "f6f7701a-28c1-e411-9469-126b3844335e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-purchase-order?${params}`, {
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
| `id` | string | yes | The Acumatica entity ID (GUID) returned in the record's id field. Example: `f6f7701a-28c1-e411-9469-126b3844335e`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated entity fields to return. Example: `OrderNbr,Type,Status,Vendor`. |
| `expand` | string | no | Comma-separated detail or linked entities to expand. Example: `Details`. |
| `custom` | string | no | Comma-separated custom fields to return. Example: `OrderNbr,Status`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {
        "files:put": "https://example.com",
        "self": "https://example.com"
      },
      "BaseCurrencyID": {
        "value": "string"
      },
      "Branch": {
        "value": "string"
      },
      "ControlTotal": {
        "value": 1
      },
      "CurrencyEffectiveDate": {
        "value": "string"
      },
      "CurrencyID": {
        "value": "string"
      },
      "CurrencyRate": {
        "value": 1
      },
      "CurrencyReciprocalRate": {
        "value": 1
      },
      "Date": {
        "value": "string"
      },
      "Description": {
        "value": "string"
      },
      "Hold": {
        "value": true
      },
      "id": "string",
      "LastModifiedDateTime": {
        "value": "string"
      },
      "LineTotal": {
        "value": 1
      },
      "Location": {
        "value": "string"
      },
      "note": {
        "value": "string"
      },
      "OrderNbr": {
        "value": "string"
      },
      "OrderTotal": {
        "value": 1
      },
      "Owner": {
        "value": "string"
      },
      "Project": {
        "value": "string"
      },
      "PromisedOn": {
        "value": "string"
      },
      "rowNumber": 1,
      "Status": {
        "value": "string"
      },
      "TaxTotal": {
        "value": 1
      },
      "Terms": {
        "value": "string"
      },
      "Type": {
        "value": "string"
      },
      "VendorID": {
        "value": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links.files:put` | string |  |
| `_links.self` | string |  |
| `BaseCurrencyID.value` | string |  |
| `Branch.value` | string |  |
| `ControlTotal.value` | number |  |
| `CurrencyEffectiveDate.value` | string |  |
| `CurrencyID.value` | string |  |
| `CurrencyRate.value` | number |  |
| `CurrencyReciprocalRate.value` | number |  |
| `Date.value` | string |  |
| `Description.value` | string |  |
| `Hold.value` | boolean |  |
| `id` | string |  |
| `LastModifiedDateTime.value` | string |  |
| `LineTotal.value` | number |  |
| `Location.value` | string |  |
| `note.value` | string |  |
| `OrderNbr.value` | string |  |
| `OrderTotal.value` | number |  |
| `Owner.value` | string |  |
| `Project.value` | string |  |
| `PromisedOn.value` | string |  |
| `rowNumber` | number |  |
| `Status.value` | string |  |
| `TaxTotal.value` | number |  |
| `Terms.value` | string |  |
| `Type.value` | string |  |
| `VendorID.value` | string |  |

## Native endpoint

Through the native Acumatica API, this operation is `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/PurchaseOrder/:id` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-purchase-order.md) for the provider-specific parameters and requirements.

