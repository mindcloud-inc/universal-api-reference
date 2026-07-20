# Zillow Public Records: List parcel transactions

Retrieves parcel transactions from Zillow Public Records by parcel ID.

```
GET https://connect.mindcloud.co/v1/universal/zillowPublicRecords/latest/actions/list-parcel-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zillow Public Records `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowPublicRecords/latest/actions/list-parcel-transactions?connectionId=$CONNECTION_ID&parcelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "parcelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zillowPublicRecords/latest/actions/list-parcel-transactions?${params}`, {
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
| `parcelId` | string | yes | Bridge parcel identifier used to fetch transaction history for a parcel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buyerName": [
        "Ava Chen"
      ],
      "documentDate": "2026-05-07T12:00:00.000Z",
      "documentType": "string",
      "documentTypeCode": "string",
      "effectiveDate": "2026-05-07T12:00:00.000Z",
      "fips": "string",
      "id": 1,
      "lenderName": "Ava Chen",
      "loanAmount": 1,
      "parcels": [
        {}
      ],
      "recordingBookNumber": "string",
      "recordingDate": "2026-05-07T12:00:00.000Z",
      "recordingPageNumber": "string",
      "recordType": "string",
      "salesPrice": 1,
      "sellerName": [
        "Ava Chen"
      ],
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buyerName` | array<string> | Buyer names. |
| `documentDate` | date | Document creation date. |
| `documentType` | string | Short description of the document type. |
| `documentTypeCode` | string | Document type code. |
| `effectiveDate` | date | Date the transaction takes effect. |
| `fips` | string | Five-digit county FIPS code. |
| `id` | number | Unique transaction identifier. |
| `lenderName` | string | Lender name. |
| `loanAmount` | number | Loan amount. |
| `parcels` | array<object> | Parcel records linked to the transaction. |
| `recordingBookNumber` | string | Recording book number. |
| `recordingDate` | date | Date the transaction was recorded. |
| `recordingPageNumber` | string | Recording page number. |
| `recordType` | string | Record type code. |
| `salesPrice` | number | Sale price. |
| `sellerName` | array<string> | Seller names. |
| `state` | string | Two-character state abbreviation. |

## Native endpoint

Through the native Zillow Public Records API, this operation is `GET /pub/parcels/:parcelId/transactions` (base URL `https://api.bridgedataoutput.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-parcel-transactions.md) for the provider-specific parameters and requirements.

