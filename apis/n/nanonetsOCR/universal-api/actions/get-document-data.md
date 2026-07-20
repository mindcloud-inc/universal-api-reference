# Nanonets OCR: Get Document Data



```
GET https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/get-document-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nanonets OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/get-document-data?connectionId=$CONNECTION_ID&workflowId=Select%20a%20workflow&documentId=485aa6b0-a04e-423d-8f45-2f184819766b" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "Select a workflow",
  "documentId": "485aa6b0-a04e-423d-8f45-2f184819766b"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/get-document-data?${params}`, {
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
| `workflowId` | list | yes | Workflow identifier. Example: `Select a workflow`. |
| `documentId` | string | yes | Document identifier. Example: `485aa6b0-a04e-423d-8f45-2f184819766b`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedReviewers": {},
      "documentId": "string",
      "originalDocumentName": "Ava Chen",
      "pages": [
        {
          "data": {
            "fields": {
              "buyerAddress": [
                {
                  "bbox": [
                    1
                  ],
                  "confidence": 1,
                  "fieldDataId": "string",
                  "isModerated": true,
                  "value": "string",
                  "verificationStatus": "string"
                }
              ],
              "buyerName": [
                {
                  "bbox": [
                    1
                  ],
                  "confidence": 1,
                  "fieldDataId": "Ava Chen",
                  "isModerated": true,
                  "value": "Ava Chen",
                  "verificationStatus": "Ava Chen"
                }
              ],
              "currency": [
                {
                  "bbox": [
                    1
                  ],
                  "confidence": 1,
                  "fieldDataId": "string",
                  "isModerated": true,
                  "value": "string",
                  "verificationStatus": "string"
                }
              ],
              "invoiceAmount": [
                {
                  "bbox": [
                    1
                  ],
                  "confidence": 1,
                  "fieldDataId": "string",
                  "isModerated": true,
                  "value": "string",
                  "verificationStatus": "string"
                }
              ],
              "invoiceDate": [
                {
                  "bbox": [
                    1
                  ],
                  "confidence": 1,
                  "fieldDataId": "string",
                  "isModerated": true,
                  "value": "string",
                  "verificationStatus": "string"
                }
              ],
              "invoiceNumber": [
                {
                  "bbox": [
                    1
                  ],
                  "confidence": 1,
                  "fieldDataId": "string",
                  "isModerated": true,
                  "value": "string",
                  "verificationStatus": "string"
                }
              ],
              "netD": [
                {
                  "bbox": [
                    1
                  ],
                  "confidence": 1,
                  "fieldDataId": "string",
                  "isModerated": true,
                  "value": "string",
                  "verificationStatus": "string"
                }
              ],
              "paymentDueDate": [
                {
                  "bbox": [
                    1
                  ],
                  "confidence": 1,
                  "fieldDataId": "string",
                  "isModerated": true,
                  "value": "string",
                  "verificationStatus": "string"
                }
              ],
              "paytoName": [
                {
                  "bbox": [
                    1
                  ],
                  "confidence": 1,
                  "fieldDataId": "Ava Chen",
                  "isModerated": true,
                  "value": "Ava Chen",
                  "verificationStatus": "Ava Chen"
                }
              ],
              "poNumber": [
                {
                  "bbox": [
                    1
                  ],
                  "confidence": 1,
                  "fieldDataId": "string",
                  "isModerated": true,
                  "value": "string",
                  "verificationStatus": "string"
                }
              ],
              "sellerEmail": [
                {
                  "bbox": [
                    1
                  ],
                  "confidence": 1,
                  "fieldDataId": "ava@example.com",
                  "isModerated": true,
                  "value": "ava@example.com",
                  "verificationStatus": "ava@example.com"
                }
              ],
              "sellerPhone": [
                {
                  "bbox": [
                    1
                  ],
                  "confidence": 1,
                  "fieldDataId": "string",
                  "isModerated": true,
                  "value": "string",
                  "verificationStatus": "string"
                }
              ],
              "subtotal": [
                {
                  "bbox": [
                    1
                  ],
                  "confidence": 1,
                  "fieldDataId": "string",
                  "isModerated": true,
                  "value": "string",
                  "verificationStatus": "string"
                }
              ],
              "totalTax": [
                {
                  "bbox": [
                    1
                  ],
                  "confidence": 1,
                  "fieldDataId": "string",
                  "isModerated": true,
                  "value": "string",
                  "verificationStatus": "string"
                }
              ],
              "totalTax%": [
                {
                  "bbox": [
                    1
                  ],
                  "confidence": 1,
                  "fieldDataId": "string",
                  "isModerated": true,
                  "value": "string",
                  "verificationStatus": "string"
                }
              ]
            },
            "tables": [
              {
                "bbox": [
                  1
                ],
                "cells": [
                  {
                    "bbox": [
                      1
                    ],
                    "cellId": "string",
                    "col": 1,
                    "header": "string",
                    "isModerated": true,
                    "row": 1,
                    "text": "string",
                    "verificationStatus": "string"
                  }
                ],
                "tableId": "string"
              }
            ]
          },
          "imageUrl": "https://example.com",
          "pageId": "string",
          "pageNumber": 1
        }
      ],
      "rawDocumentUrl": "https://example.com",
      "status": "string",
      "uploadedAt": "string",
      "verificationStage": "string",
      "verificationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedReviewers` | object |  |
| `documentId` | string |  |
| `originalDocumentName` | string |  |
| `pages[].data.fields.buyerAddress[].bbox[]` | number |  |
| `pages[].data.fields.buyerAddress[].confidence` | number |  |
| `pages[].data.fields.buyerAddress[].fieldDataId` | string |  |
| `pages[].data.fields.buyerAddress[].isModerated` | boolean |  |
| `pages[].data.fields.buyerAddress[].value` | string |  |
| `pages[].data.fields.buyerAddress[].verificationStatus` | string |  |
| `pages[].data.fields.buyerName[].bbox[]` | number |  |
| `pages[].data.fields.buyerName[].confidence` | number |  |
| `pages[].data.fields.buyerName[].fieldDataId` | string |  |
| `pages[].data.fields.buyerName[].isModerated` | boolean |  |
| `pages[].data.fields.buyerName[].value` | string |  |
| `pages[].data.fields.buyerName[].verificationStatus` | string |  |
| `pages[].data.fields.currency[].bbox[]` | number |  |
| `pages[].data.fields.currency[].confidence` | number |  |
| `pages[].data.fields.currency[].fieldDataId` | string |  |
| `pages[].data.fields.currency[].isModerated` | boolean |  |
| `pages[].data.fields.currency[].value` | string |  |
| `pages[].data.fields.currency[].verificationStatus` | string |  |
| `pages[].data.fields.invoiceAmount[].bbox[]` | number |  |
| `pages[].data.fields.invoiceAmount[].confidence` | number |  |
| `pages[].data.fields.invoiceAmount[].fieldDataId` | string |  |
| `pages[].data.fields.invoiceAmount[].isModerated` | boolean |  |
| `pages[].data.fields.invoiceAmount[].value` | string |  |
| `pages[].data.fields.invoiceAmount[].verificationStatus` | string |  |
| `pages[].data.fields.invoiceDate[].bbox[]` | number |  |
| `pages[].data.fields.invoiceDate[].confidence` | number |  |
| `pages[].data.fields.invoiceDate[].fieldDataId` | string |  |
| `pages[].data.fields.invoiceDate[].isModerated` | boolean |  |
| `pages[].data.fields.invoiceDate[].value` | string |  |
| `pages[].data.fields.invoiceDate[].verificationStatus` | string |  |
| `pages[].data.fields.invoiceNumber[].bbox[]` | number |  |
| `pages[].data.fields.invoiceNumber[].confidence` | number |  |
| `pages[].data.fields.invoiceNumber[].fieldDataId` | string |  |
| `pages[].data.fields.invoiceNumber[].isModerated` | boolean |  |
| `pages[].data.fields.invoiceNumber[].value` | string |  |
| `pages[].data.fields.invoiceNumber[].verificationStatus` | string |  |
| `pages[].data.fields.netD[].bbox[]` | number |  |
| `pages[].data.fields.netD[].confidence` | number |  |
| `pages[].data.fields.netD[].fieldDataId` | string |  |
| `pages[].data.fields.netD[].isModerated` | boolean |  |
| `pages[].data.fields.netD[].value` | string |  |
| `pages[].data.fields.netD[].verificationStatus` | string |  |
| `pages[].data.fields.paymentDueDate[].bbox[]` | number |  |
| `pages[].data.fields.paymentDueDate[].confidence` | number |  |
| `pages[].data.fields.paymentDueDate[].fieldDataId` | string |  |
| `pages[].data.fields.paymentDueDate[].isModerated` | boolean |  |
| `pages[].data.fields.paymentDueDate[].value` | string |  |
| `pages[].data.fields.paymentDueDate[].verificationStatus` | string |  |
| `pages[].data.fields.paytoName[].bbox[]` | number |  |
| `pages[].data.fields.paytoName[].confidence` | number |  |
| `pages[].data.fields.paytoName[].fieldDataId` | string |  |
| `pages[].data.fields.paytoName[].isModerated` | boolean |  |
| `pages[].data.fields.paytoName[].value` | string |  |
| `pages[].data.fields.paytoName[].verificationStatus` | string |  |
| `pages[].data.fields.poNumber[].bbox[]` | number |  |
| `pages[].data.fields.poNumber[].confidence` | number |  |
| `pages[].data.fields.poNumber[].fieldDataId` | string |  |
| `pages[].data.fields.poNumber[].isModerated` | boolean |  |
| `pages[].data.fields.poNumber[].value` | string |  |
| `pages[].data.fields.poNumber[].verificationStatus` | string |  |
| `pages[].data.fields.sellerEmail[].bbox[]` | number |  |
| `pages[].data.fields.sellerEmail[].confidence` | number |  |
| `pages[].data.fields.sellerEmail[].fieldDataId` | string |  |
| `pages[].data.fields.sellerEmail[].isModerated` | boolean |  |
| `pages[].data.fields.sellerEmail[].value` | string |  |
| `pages[].data.fields.sellerEmail[].verificationStatus` | string |  |
| `pages[].data.fields.sellerPhone[].bbox[]` | number |  |
| `pages[].data.fields.sellerPhone[].confidence` | number |  |
| `pages[].data.fields.sellerPhone[].fieldDataId` | string |  |
| `pages[].data.fields.sellerPhone[].isModerated` | boolean |  |
| `pages[].data.fields.sellerPhone[].value` | string |  |
| `pages[].data.fields.sellerPhone[].verificationStatus` | string |  |
| `pages[].data.fields.subtotal[].bbox[]` | number |  |
| `pages[].data.fields.subtotal[].confidence` | number |  |
| `pages[].data.fields.subtotal[].fieldDataId` | string |  |
| `pages[].data.fields.subtotal[].isModerated` | boolean |  |
| `pages[].data.fields.subtotal[].value` | string |  |
| `pages[].data.fields.subtotal[].verificationStatus` | string |  |
| `pages[].data.fields.totalTax[].bbox[]` | number |  |
| `pages[].data.fields.totalTax[].confidence` | number |  |
| `pages[].data.fields.totalTax[].fieldDataId` | string |  |
| `pages[].data.fields.totalTax[].isModerated` | boolean |  |
| `pages[].data.fields.totalTax[].value` | string |  |
| `pages[].data.fields.totalTax[].verificationStatus` | string |  |
| `pages[].data.fields.totalTax%[].bbox[]` | number |  |
| `pages[].data.fields.totalTax%[].confidence` | number |  |
| `pages[].data.fields.totalTax%[].fieldDataId` | string |  |
| `pages[].data.fields.totalTax%[].isModerated` | boolean |  |
| `pages[].data.fields.totalTax%[].value` | string |  |
| `pages[].data.fields.totalTax%[].verificationStatus` | string |  |
| `pages[].data.tables[].bbox[]` | number |  |
| `pages[].data.tables[].cells[].bbox[]` | number |  |
| `pages[].data.tables[].cells[].cellId` | string |  |
| `pages[].data.tables[].cells[].col` | number |  |
| `pages[].data.tables[].cells[].header` | string |  |
| `pages[].data.tables[].cells[].isModerated` | boolean |  |
| `pages[].data.tables[].cells[].row` | number |  |
| `pages[].data.tables[].cells[].text` | string |  |
| `pages[].data.tables[].cells[].verificationStatus` | string |  |
| `pages[].data.tables[].tableId` | string |  |
| `pages[].imageUrl` | string |  |
| `pages[].pageId` | string |  |
| `pages[].pageNumber` | number |  |
| `rawDocumentUrl` | string |  |
| `status` | string |  |
| `uploadedAt` | string |  |
| `verificationStage` | string |  |
| `verificationStatus` | string |  |

## Native endpoint

Through the native Nanonets OCR API, this operation is `GET /workflows/:workflow_id/documents/:document_id` (base URL `https://app.nanonets.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-data.md) for the provider-specific parameters and requirements.

