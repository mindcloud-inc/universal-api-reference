# Acumatica: Get Invoice



```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-invoice?connectionId=$CONNECTION_ID&id=671e3b2c-d87f-e411-beca-00b56d0561c2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "671e3b2c-d87f-e411-beca-00b56d0561c2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-invoice?${params}`, {
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
| `id` | string | yes | The Acumatica entity ID (GUID) returned in the record's id field. Example: `671e3b2c-d87f-e411-beca-00b56d0561c2`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated entity fields to return. Example: `ReferenceNbr,Type,Status,Customer`. |
| `expand` | string | no | Comma-separated detail or linked entities to expand. Example: `Details,Applications`. |
| `custom` | string | no | Comma-separated custom fields to return. Example: `ReferenceNbr,Status`. |

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
      "Amount": {
        "value": 1
      },
      "Balance": {
        "value": 1
      },
      "BillingPrinted": {
        "value": true
      },
      "BillToContactOverride": {
        "value": true
      },
      "CreatedDateTime": {
        "value": "string"
      },
      "Customer": {
        "value": "string"
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
      "LinkARAccount": {
        "value": "https://example.com"
      },
      "LinkBranch": {
        "value": "https://example.com"
      },
      "LocationID": {
        "value": "string"
      },
      "note": {
        "value": "string"
      },
      "PostPeriod": {
        "value": "string"
      },
      "Project": {
        "value": "string"
      },
      "ReferenceNbr": {
        "value": "string"
      },
      "rowNumber": 1,
      "ShipToContactOverride": {
        "value": true
      },
      "Status": {
        "value": "string"
      },
      "TaxTotal": {
        "value": 1
      },
      "Type": {
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
| `Amount.value` | number |  |
| `Balance.value` | number |  |
| `BillingPrinted.value` | boolean |  |
| `BillToContactOverride.value` | boolean |  |
| `CreatedDateTime.value` | string |  |
| `Customer.value` | string |  |
| `Date.value` | string |  |
| `Description.value` | string |  |
| `Hold.value` | boolean |  |
| `id` | string |  |
| `LastModifiedDateTime.value` | string |  |
| `LinkARAccount.value` | string |  |
| `LinkBranch.value` | string |  |
| `LocationID.value` | string |  |
| `note.value` | string |  |
| `PostPeriod.value` | string |  |
| `Project.value` | string |  |
| `ReferenceNbr.value` | string |  |
| `rowNumber` | number |  |
| `ShipToContactOverride.value` | boolean |  |
| `Status.value` | string |  |
| `TaxTotal.value` | number |  |
| `Type.value` | string |  |

## Native endpoint

Through the native Acumatica API, this operation is `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Invoice/:id` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

