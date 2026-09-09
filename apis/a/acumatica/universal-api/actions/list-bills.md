# Acumatica: List Bills



```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-bills
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-bills?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-bills?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated entity fields to return. Example: `ReferenceNbr,Type,Status,Vendor`. |
| `expand` | string | no | Comma-separated detail or linked entities to expand. Example: `Details,Applications`. |
| `filter` | string | no | Acumatica OData filter expression used to qualify returned records. Example: `Status eq 'Open'`. |
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
      "ApprovedForPayment": {
        "value": true
      },
      "Balance": {
        "value": 1
      },
      "BranchID": {
        "value": "string"
      },
      "CashAccount": {
        "value": "string"
      },
      "CurrencyID": {
        "value": "string"
      },
      "Date": {
        "value": "string"
      },
      "Description": {
        "value": "string"
      },
      "DueDate": {
        "value": "string"
      },
      "Hold": {
        "value": true
      },
      "id": "string",
      "LastModifiedDateTime": {
        "value": "string"
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
      "Vendor": {
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
| `ApprovedForPayment.value` | boolean |  |
| `Balance.value` | number |  |
| `BranchID.value` | string |  |
| `CashAccount.value` | string |  |
| `CurrencyID.value` | string |  |
| `Date.value` | string |  |
| `Description.value` | string |  |
| `DueDate.value` | string |  |
| `Hold.value` | boolean |  |
| `id` | string |  |
| `LastModifiedDateTime.value` | string |  |
| `LocationID.value` | string |  |
| `note.value` | string |  |
| `PostPeriod.value` | string |  |
| `Project.value` | string |  |
| `ReferenceNbr.value` | string |  |
| `rowNumber` | number |  |
| `Status.value` | string |  |
| `TaxTotal.value` | number |  |
| `Terms.value` | string |  |
| `Type.value` | string |  |
| `Vendor.value` | string |  |

## Native endpoint

Through the native Acumatica API, this operation is `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Bill` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-bills.md) for the provider-specific parameters and requirements.

