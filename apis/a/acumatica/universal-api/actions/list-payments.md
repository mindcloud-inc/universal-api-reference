# Acumatica: List Payments



```
GET https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-payments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/list-payments?${params}`, {
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
| `select` | string | no | Comma-separated entity fields to return. Example: `ReferenceNbr,Type,Status,Customer`. |
| `expand` | string | no | Comma-separated detail or linked entities to expand. Example: `ApplicationHistory`. |
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
      "ApplicationDate": {
        "value": "string"
      },
      "Branch": {
        "value": "string"
      },
      "CurrencyID": {
        "value": "string"
      },
      "CustomerID": {
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
      "note": {
        "value": "string"
      },
      "PaymentAmount": {
        "value": 1
      },
      "ReferenceNbr": {
        "value": "string"
      },
      "rowNumber": 1,
      "SaveCard": {
        "value": true
      },
      "Status": {
        "value": "string"
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
| `ApplicationDate.value` | string |  |
| `Branch.value` | string |  |
| `CurrencyID.value` | string |  |
| `CustomerID.value` | string |  |
| `Description.value` | string |  |
| `Hold.value` | boolean |  |
| `id` | string |  |
| `LastModifiedDateTime.value` | string |  |
| `note.value` | string |  |
| `PaymentAmount.value` | number |  |
| `ReferenceNbr.value` | string |  |
| `rowNumber` | number |  |
| `SaveCard.value` | boolean |  |
| `Status.value` | string |  |
| `Type.value` | string |  |

## Native endpoint

Through the native Acumatica API, this operation is `GET /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/Payment` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payments.md) for the provider-specific parameters and requirements.

