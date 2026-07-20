# Fatture in Cloud: List Issued Documents

Retrieves issued documents from Fatture in Cloud.

```
GET https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/list-issued-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fatture in Cloud `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/list-issued-documents?connectionId=$CONNECTION_ID&limit=25&offset=0&companyId=1&type=credit_note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "companyId": "1",
  "type": "credit_note"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/list-issued-documents?${params}`, {
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
| `companyId` | number | yes | The ID of the company. |
| `type` | list | yes | The type of the issued document. One of: `credit_note`, `delivery_note`, `invoice`, `order`, `proforma`, `quote`, `receipt`, `self_own_invoice`, `self_supplier_invoice`, `supplier_order`, `work_report`. |
| `fields` | string | no | List of comma-separated fields. |
| `fieldset` | list | no | Name of the fieldset. One of: `basic`, `detailed`, `fic_view`. |
| `q` | string | no | Query for filtering the results. |
| `inclusive` | number | no | (Only for type = delivery_notes) Include invoices delivery notes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountDueDiscount": 1,
      "amountGross": 1,
      "amountNet": 1,
      "amountVat": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "entity": {
        "addressCity": "string",
        "addressExtra": "string",
        "addressPostalCode": "string",
        "addressProvince": "string",
        "addressStreet": "string",
        "certifiedEmail": "ava@example.com",
        "country": "string",
        "eiCode": "string",
        "id": 1,
        "name": "Ava Chen",
        "taxCode": "string",
        "vatNumber": "string"
      },
      "id": 1,
      "nextDueDate": "2026-05-07T12:00:00.000Z",
      "number": 1,
      "numeration": "string",
      "subject": "string",
      "type": "string",
      "url": "https://example.com",
      "visibleSubject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountDueDiscount` | number |  |
| `amountGross` | number |  |
| `amountNet` | number |  |
| `amountVat` | number |  |
| `date` | date |  |
| `entity.addressCity` | string |  |
| `entity.addressExtra` | string |  |
| `entity.addressPostalCode` | string |  |
| `entity.addressProvince` | string |  |
| `entity.addressStreet` | string |  |
| `entity.certifiedEmail` | string |  |
| `entity.country` | string |  |
| `entity.eiCode` | string |  |
| `entity.id` | number |  |
| `entity.name` | string |  |
| `entity.taxCode` | string |  |
| `entity.vatNumber` | string |  |
| `id` | number |  |
| `nextDueDate` | date |  |
| `number` | number |  |
| `numeration` | string |  |
| `subject` | string |  |
| `type` | string |  |
| `url` | string |  |
| `visibleSubject` | string |  |

## Native endpoint

Through the native Fatture in Cloud API, this operation is `GET /c/:company_id/issued_documents` (base URL `https://api-v2.fattureincloud.it`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-issued-documents.md) for the provider-specific parameters and requirements.

