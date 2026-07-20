# Veryfi: Update a Check

Updates an existing check in Veryfi.

```
PUT https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-checks-document-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-checks-document-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "amount": "string",
  "amountText": {},
  "bankAddress": {},
  "bankName": {},
  "fractionalRoutingNumber": {},
  "micr": "string",
  "checkNumber": {},
  "date": {},
  "isSigned": {},
  "memo": {},
  "endorsement": "string",
  "payerAddress": {},
  "payerName": {},
  "receiverAddress": {},
  "receiverName": {},
  "currencyCode": {},
  "checkType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-checks-document-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string",
    "amount": "string",
    "amountText": {},
    "bankAddress": {},
    "bankName": {},
    "fractionalRoutingNumber": {},
    "micr": "string",
    "checkNumber": {},
    "date": {},
    "isSigned": {},
    "memo": {},
    "endorsement": "string",
    "payerAddress": {},
    "payerName": {},
    "receiverAddress": {},
    "receiverName": {},
    "currencyCode": {},
    "checkType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes |  |
| `externalId` | string | no | Possible values: non-empty Deprecated 2025-01-09, use meta.external_id instead. |
| `meta` | string | no | Possible values: non-empty Possible values: non-empty Default value: `` |
| `amount` | string | yes | Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: > 0 Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `amountText` | object | yes | Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: non-empty The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `bankAddress` | object | yes | Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 4 characters The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `bankName` | object | yes | Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: non-empty The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `fractionalRoutingNumber` | object | yes | Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: non-empty The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `micr` | string | yes | Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 4 characters The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 4 characters The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: non-empty The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 4 characters The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 4 characters The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 3 characters The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: non-empty and <= 4 characters The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `checkNumber` | object | yes | Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: non-empty The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `date` | object | yes | Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `isSigned` | object | yes |  |
| `memo` | object | yes | Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: non-empty The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `endorsement` | string | yes |  |
| `payerAddress` | object | yes | Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 4 characters The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `payerName` | object | yes | Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: non-empty The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `receiverAddress` | object | yes | Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 4 characters The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `receiverName` | object | yes | Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: non-empty The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `currencyCode` | object | yes | The currency code in ISO 4217 format. Possible values: [ FJD , JMD , AUD , RSD , VEF , JEP , ILS , CZK , USD , SHP , BZD , HKD , CLP , HTG , BRL , HNL , MNT , NOK , SZL , EEK , DOP , MYR , SYP , IMP , THB , ZAR , HRK , EGP , MXN , BHD , IDR , LRD , TRL , TRY , CHF , MVR , BBD , SVC , ALL , BMD , UAH , EUR , YER , GBP , XCD , AWG , KPW , PHP , UZS , VND , OMR , KZT , PLN , MUR , TVD , UYU , PEN , MKD , BSD , KHR , GHC , KYD , HUF , KRW , IQD , NGN , SAR , GTQ , ZWD , BND , ISK , GEL , CAD , SOS , LAK , ARS , UGX , BWP , RUB , TWD , LTL , LKR , CRC , GGP , PYG , BGN , FKP , SCR , AED , QAR , AZN , IRR , NAD , SBD , DKK , AMD , GNF , GYD , LBP , LVL , TTD , SRD , KWD , MZN , NPR , CUP , INR , BAM , NZD , SEK , MOP , PKR , CNY , NIO , JPY , AFN , KGS , SGD , ANG , BYR , LSL , BOB , GIP , RON , COP , PAB ] |
| `checkType` | string | yes | The type of the check like personal_check, government_check, etc. Possible values: [ bank_draft , bill_pay_draft , business_check , cashiers_check , government_check , money_order , personal_check , starter_check , teller_check ] |
| `customFields` | object | no | A user-defined dictionary that contains all the custom fields generated by applying specific rules and regular expressions to the extracted data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": {},
      "amount_text": {},
      "bank_address": {},
      "bank_name": {},
      "check_number": {},
      "check_type": "string",
      "created_date": "string",
      "currency_code": "string",
      "custom_fields": "string",
      "date": {},
      "endorsement": {},
      "external_id": "string",
      "fractional_routing_number": {},
      "id": 1,
      "img_thumbnail_url": "https://example.com",
      "is_signed": {},
      "memo": {},
      "meta": {},
      "micr": {},
      "payer_address": {},
      "payer_name": {},
      "pdf_url": "https://example.com",
      "receiver_address": {},
      "receiver_name": {},
      "routing_from_fractional": {},
      "text": "string",
      "updated_date": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | object |  |
| `amount_text` | object |  |
| `bank_address` | object |  |
| `bank_name` | object |  |
| `check_number` | object |  |
| `check_type` | string |  |
| `created_date` | string |  |
| `currency_code` | string |  |
| `custom_fields` | string |  |
| `date` | object |  |
| `endorsement` | object |  |
| `external_id` | string |  |
| `fractional_routing_number` | object |  |
| `id` | number |  |
| `img_thumbnail_url` | string |  |
| `is_signed` | object |  |
| `memo` | object |  |
| `meta` | object |  |
| `micr` | object |  |
| `payer_address` | object |  |
| `payer_name` | object |  |
| `pdf_url` | string |  |
| `receiver_address` | object |  |
| `receiver_name` | object |  |
| `routing_from_fractional` | object |  |
| `text` | string |  |
| `updated_date` | string |  |

## Native endpoint

Through the native Veryfi API, this operation is `PUT /api/v8/partner/checks/:document_id` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-api-v8-partner-checks-document-id.md) for the provider-specific parameters and requirements.

