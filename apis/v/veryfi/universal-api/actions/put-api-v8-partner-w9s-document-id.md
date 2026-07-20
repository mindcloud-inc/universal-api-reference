# Veryfi: Update a W-9

Updates an existing W-9 in Veryfi.

```
PUT https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-w9s-document-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-w9s-document-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "accountNumbers": {},
  "address1": {},
  "address2": {},
  "businessName": {},
  "cCorp": "string",
  "ein": 1,
  "exemptPayeeCode": {},
  "exemption": {},
  "individual": "string",
  "llc": "string",
  "llcType": "string",
  "name": {},
  "otherDescription": {},
  "other": "string",
  "partnership": "string",
  "requester": {},
  "sCorp": "string",
  "signatureDate": {},
  "signature": "string",
  "ssn": 1,
  "trustEstate": "string",
  "3bForeign": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-w9s-document-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string",
    "accountNumbers": {},
    "address1": {},
    "address2": {},
    "businessName": {},
    "cCorp": "string",
    "ein": 1,
    "exemptPayeeCode": {},
    "exemption": {},
    "individual": "string",
    "llc": "string",
    "llcType": "string",
    "name": {},
    "otherDescription": {},
    "other": "string",
    "partnership": "string",
    "requester": {},
    "sCorp": "string",
    "signatureDate": {},
    "signature": "string",
    "ssn": 1,
    "trustEstate": "string",
    "3bForeign": "string"
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
| `accountNumbers` | object | yes | The account numbers to a bank or brokerage account on Line 7 of the W-9. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 4 characters The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `address1` | object | yes | The address (number, street, and apt. or suite no.) on Line 5 of the W-9. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 4 characters The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `address2` | object | yes | The city, state, and zip on Line 6 of the W-9. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 4 characters The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `businessName` | object | yes | The business name on Line 2 of the W-9. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 4 characters The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `cCorp` | string | yes | A boolean indicating whether or not the LLC is identified as a C Corp and was checked in Box 3 of the W-9. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `ein` | number | yes | The Employer Identification Number (EIN) in Part I - Taxpayer Identification Number (TIN) on the W-9. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 9 characters The SSN/EIN value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `exemptPayeeCode` | object | yes | The exemption payee code in Box 4 of the W-9. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: non-empty The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `exemption` | object | yes | The exemption in Box 4 of the W-9. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: non-empty The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `individual` | string | yes | A boolean indicating whether or not Individual was checked in Box 3 of the W-9. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `llc` | string | yes | A boolean indicating whether or not Limited Liability Company was checked in Box 3 of the W-9. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `llcType` | string | yes | The tax classification found in Box 3 of the W-9. Possible values: <= 1 The score shows how confident the model is that the predicted value belongs to the field. See confidence scores explained for more information. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer Possible values: <= 1 The score which shows how confident the model in recognizing value symbols. See confidence scores explained for more information. Possible values: [ 0 , 90 , 180 , 270 ] The angle of rotation of the document in degrees. Possible values: [ C , S , P ] The tax classification found in Box 3 of the W-9. |
| `name` | object | yes | The full name found on Line 1 of the W-9. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 4 characters The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `otherDescription` | object | yes | The comments or description found on the Other line in Box 3 of the W-9. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 4 characters The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `other` | string | yes | A boolean indicating whether or not the Other box was checked in Box 3 of the W-9. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `partnership` | string | yes | A boolean indicating whether or not the LLC is identified as a Partnership and was checked in Box 3 of the W-9. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `requester` | object | yes | The requestor's name and address in the Box to the right of Line 5 of the W-9 Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 4 characters The value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `sCorp` | string | yes | A boolean indicating whether or not the LLC is identified as a S Corp and was checked in Box 3 of the W-9. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `signatureDate` | object | yes | The date found on the Sign Here line under Part II - Certification of the W-9. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `signature` | string | yes | The signature found on the Sign Here line under Part II - Certification of the W-9. Machine-printed text in signature area is treated as a signature. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `ssn` | number | yes | The number found on Part I Taxpayer Identification Number (TIN) under Social Security Number of the W-9. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 9 characters The SSN/EIN value to update Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `trustEstate` | string | yes | A boolean indicating whether or not Trust/estate was checked in Box 3 of the W-9. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |
| `3bForeign` | string | yes | Foreign ownership interest. Returns null if the field did not appear on the document. Possible values: >= 8 , <= 8 An array containing (x,y) coordinates in the format [x1,y1,x2,y2,x3,y3,x4,y4]` for skewed images and handwritten fields. The bounding region is more precise than bounding box, otherwise it's the same. Possible values: >= 5 , <= 5 An array containing relative coordinates in the format [page_number,x1,y1,x2,y2] for the extracted field from img_url before any rotation. number integer |

## Response

```json
{
  "success": true,
  "data": [
    {
      "3b_foreign": {},
      "account_numbers": {},
      "address1": {},
      "address2": {},
      "business_name": {},
      "c_corp": {},
      "created_date": "string",
      "ein": {},
      "exempt_payee_code": {},
      "exemption": {},
      "external_id": "string",
      "id": 1,
      "img_thumbnail_url": "https://example.com",
      "individual": {},
      "llc": {},
      "llc_type": {},
      "meta": {},
      "name": {},
      "other": {},
      "other_description": {},
      "parsed_address": {},
      "partnership": {},
      "pdf_url": "https://example.com",
      "requester": {},
      "s_corp": {},
      "signature": {},
      "signature_date": {},
      "ssn": {},
      "text": "string",
      "trust_estate": {},
      "updated_date": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `3b_foreign` | object |  |
| `account_numbers` | object |  |
| `address1` | object |  |
| `address2` | object |  |
| `business_name` | object |  |
| `c_corp` | object |  |
| `created_date` | string |  |
| `ein` | object |  |
| `exempt_payee_code` | object |  |
| `exemption` | object |  |
| `external_id` | string |  |
| `id` | number |  |
| `img_thumbnail_url` | string |  |
| `individual` | object |  |
| `llc` | object |  |
| `llc_type` | object |  |
| `meta` | object |  |
| `name` | object |  |
| `other` | object |  |
| `other_description` | object |  |
| `parsed_address` | object |  |
| `partnership` | object |  |
| `pdf_url` | string |  |
| `requester` | object |  |
| `s_corp` | object |  |
| `signature` | object |  |
| `signature_date` | object |  |
| `ssn` | object |  |
| `text` | string |  |
| `trust_estate` | object |  |
| `updated_date` | string |  |

## Native endpoint

Through the native Veryfi API, this operation is `PUT /api/v8/partner/w9s/:document_id` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-api-v8-partner-w9s-document-id.md) for the provider-specific parameters and requirements.

