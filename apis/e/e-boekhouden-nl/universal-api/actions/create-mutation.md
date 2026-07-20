# e-Boekhouden.nl: Create Mutation

Creates a new mutation in e-Boekhouden.nl.

```
POST https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/create-mutation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Boekhouden.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/create-mutation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "date": "2026-05-07T12:00:00.000Z",
  "ledgerId": 1,
  "rows[].vatCode": "string",
  "rows[].amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/e-boekhouden-nl/latest/actions/create-mutation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "date": "2026-05-07T12:00:00.000Z",
    "ledgerId": 1,
    "rows[].vatCode": "string",
    "rows[].amount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | A list of mutation types is displayed below. \| Value \| Description \| \|---\|---\| \| 1 \| Invoice received \| \| 2 \| Invoice sent \| \| 3 \| Invoice payment received \| \| 4 \| Invoice payment sent \| \| 5 \| Money received \| \| 6 \| Money sent \| \| 7 \| General journal entry \| |
| `date` | date | yes | The date of the mutation. Error codes MUT_003 Date is missing. |
| `ledgerId` | number | yes | The ledger ID of the mutation. Error codes MUTA_001 Ledger id is missing. MUT_007 Unknown ledger for mutation. |
| `invoiceNumber` | string | no | The invoice number of the mutation. Error codes MUT_018 Invoice number is too long. MUT_019 Invoice number already exists. MUT_002 Invoice number is missing. |
| `entryNumber` | string | no | The entry of the mutation. |
| `termOfPayment` | number | no | The term of payment from `date`, in days. Error codes MUT_016 Term of payment is prohibited. |
| `checkPaymentReference` | boolean | no | If true, the provided `paymentReference` will be validated for uniqueness. |
| `paymentReference` | string | no | The payment reference of the mutation. |
| `inExVat` | string | no | Indicates if the amount on mutation rows is including (`IN`) or excluding (`EX`) VAT. The corresponding value will be calculated based on the VAT code. Error codes MUT_017 In/Ex VAT must be 'IN' or 'EX'. MUTA_005 In/Ex VAT is missing. |
| `description` | string | no | The description of the mutation. |
| `relationId` | number | no | The relation id of the mutation. Error codes MUT_012 Relation is missing. MUT_013 Relation not found. |
| `rows[].ledgerId` | number | no | The ledger ID of the row. Required in combination with `type`: 1, 2, 5, 6, 7. For `type` 1, 2, 5, 6 ledger cannot be in the category: `FIN`, `CRED`, `DEB`. For `type` 7 ledger can be any. Error codes MUTA_004 Ledger ID for row is missing. MUT_007 Unknown ledger for mutation. MUT_104 Unknown ledger for row. MUT_106 Invalid ledger category for row. |
| `rows[].vatCode` | string | yes | A list of VAT codes is displayed below. \| Value \| Description \| \|---\|---\| \| HOOG_VERK_21 \| For selling with 21% VAT. \| \| LAAG_VERK_9 \| For selling with 9% VAT. \| \| VERL_VERK \| For selling with reverse-charging 21% VAT. \| \| VERL_VERK_L9 \| For selling with reverse-charging 9% VAT. \| \| AFW \| VAT percentage is unspecified. Price values will be used \| \| BU_EU_VERK \| Deliveries outside the EU, 0% VAT. \| \| BI_EU_VERK \| Goods inside the EU, 0% VAT. \| \| BI_EU_VERK_D \| Services inside the EU, 0% VAT. \| \| AFST_VERK \| Distance sales inside the EU, 0% VAT. \| \| LAAG_INK_9 \| For buying with 9% VAT. \| \| HOOG_INK_21 \| For buying with 21% VAT. \| \| VERL_INK \| For buying with reverse-charging VAT. \| \| AFW_VERK \| For selling with unspecified VAT percentage. Price values will be used. \| \| BU_EU_INK \| For buying goods/services from outside the EU, 0% VAT. \| \| BI_EU_INK \| For buying goods/services from inside the EU, 0% VAT. \| \| GEEN \| No VAT. \| |
| `rows[].vatAmount` | number | no | The VAT amount of the row. Only use in combination with vatCode: 'AFW_VERK' or 'AFW'. Only applicable for NL. |
| `rows[].costCenterId` | number | no | The cost center id of the row. |
| `rows[].amount` | number | yes | The amount of the row. This value includes or excludes VAT depending on the `inExVat` value of the mutation. |
| `rows[].description` | string | no | The description of the row. |
| `rows[].invoiceNumber` | string | no | The invoice number of the row. Required for type 'Invoice payment received' and 'Invoice payment sent'. Error codes MUT_115 Invoice not found. MUT_120 Invoice number is missing. |
| `rows[].relationId` | number | no | The relation id of the row. Error codes MUT_112 Relation is missing. MUT_113 Relation not found. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native e-Boekhouden.nl API returns.

## Native endpoint

Through the native e-Boekhouden.nl API, this operation is `POST /v1/mutation` (base URL `https://api.e-boekhouden.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mutation.md) for the provider-specific parameters and requirements.

