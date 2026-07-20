# Nanonets OCR: Get Page Data



```
GET https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/get-page-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nanonets OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/get-page-data?connectionId=$CONNECTION_ID&workflowId=Select%20a%20workflow&documentId=485aa6b0-a04e-423d-8f45-2f184819766b&pageId=3880be00-2240-11f1-a926-66917427366e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "Select a workflow",
  "documentId": "485aa6b0-a04e-423d-8f45-2f184819766b",
  "pageId": "3880be00-2240-11f1-a926-66917427366e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/get-page-data?${params}`, {
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
| `pageId` | string | yes | Page identifier. Example: `3880be00-2240-11f1-a926-66917427366e`. |

## Response

```json
{
  "success": true,
  "data": [
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.fields.buyerAddress[].bbox[]` | number |  |
| `data.fields.buyerAddress[].confidence` | number |  |
| `data.fields.buyerAddress[].fieldDataId` | string |  |
| `data.fields.buyerAddress[].isModerated` | boolean |  |
| `data.fields.buyerAddress[].value` | string |  |
| `data.fields.buyerAddress[].verificationStatus` | string |  |
| `data.fields.buyerName[].bbox[]` | number |  |
| `data.fields.buyerName[].confidence` | number |  |
| `data.fields.buyerName[].fieldDataId` | string |  |
| `data.fields.buyerName[].isModerated` | boolean |  |
| `data.fields.buyerName[].value` | string |  |
| `data.fields.buyerName[].verificationStatus` | string |  |
| `data.fields.currency[].bbox[]` | number |  |
| `data.fields.currency[].confidence` | number |  |
| `data.fields.currency[].fieldDataId` | string |  |
| `data.fields.currency[].isModerated` | boolean |  |
| `data.fields.currency[].value` | string |  |
| `data.fields.currency[].verificationStatus` | string |  |
| `data.fields.invoiceAmount[].bbox[]` | number |  |
| `data.fields.invoiceAmount[].confidence` | number |  |
| `data.fields.invoiceAmount[].fieldDataId` | string |  |
| `data.fields.invoiceAmount[].isModerated` | boolean |  |
| `data.fields.invoiceAmount[].value` | string |  |
| `data.fields.invoiceAmount[].verificationStatus` | string |  |
| `data.fields.invoiceDate[].bbox[]` | number |  |
| `data.fields.invoiceDate[].confidence` | number |  |
| `data.fields.invoiceDate[].fieldDataId` | string |  |
| `data.fields.invoiceDate[].isModerated` | boolean |  |
| `data.fields.invoiceDate[].value` | string |  |
| `data.fields.invoiceDate[].verificationStatus` | string |  |
| `data.fields.invoiceNumber[].bbox[]` | number |  |
| `data.fields.invoiceNumber[].confidence` | number |  |
| `data.fields.invoiceNumber[].fieldDataId` | string |  |
| `data.fields.invoiceNumber[].isModerated` | boolean |  |
| `data.fields.invoiceNumber[].value` | string |  |
| `data.fields.invoiceNumber[].verificationStatus` | string |  |
| `data.fields.netD[].bbox[]` | number |  |
| `data.fields.netD[].confidence` | number |  |
| `data.fields.netD[].fieldDataId` | string |  |
| `data.fields.netD[].isModerated` | boolean |  |
| `data.fields.netD[].value` | string |  |
| `data.fields.netD[].verificationStatus` | string |  |
| `data.fields.paymentDueDate[].bbox[]` | number |  |
| `data.fields.paymentDueDate[].confidence` | number |  |
| `data.fields.paymentDueDate[].fieldDataId` | string |  |
| `data.fields.paymentDueDate[].isModerated` | boolean |  |
| `data.fields.paymentDueDate[].value` | string |  |
| `data.fields.paymentDueDate[].verificationStatus` | string |  |
| `data.fields.paytoName[].bbox[]` | number |  |
| `data.fields.paytoName[].confidence` | number |  |
| `data.fields.paytoName[].fieldDataId` | string |  |
| `data.fields.paytoName[].isModerated` | boolean |  |
| `data.fields.paytoName[].value` | string |  |
| `data.fields.paytoName[].verificationStatus` | string |  |
| `data.fields.poNumber[].bbox[]` | number |  |
| `data.fields.poNumber[].confidence` | number |  |
| `data.fields.poNumber[].fieldDataId` | string |  |
| `data.fields.poNumber[].isModerated` | boolean |  |
| `data.fields.poNumber[].value` | string |  |
| `data.fields.poNumber[].verificationStatus` | string |  |
| `data.fields.sellerEmail[].bbox[]` | number |  |
| `data.fields.sellerEmail[].confidence` | number |  |
| `data.fields.sellerEmail[].fieldDataId` | string |  |
| `data.fields.sellerEmail[].isModerated` | boolean |  |
| `data.fields.sellerEmail[].value` | string |  |
| `data.fields.sellerEmail[].verificationStatus` | string |  |
| `data.fields.sellerPhone[].bbox[]` | number |  |
| `data.fields.sellerPhone[].confidence` | number |  |
| `data.fields.sellerPhone[].fieldDataId` | string |  |
| `data.fields.sellerPhone[].isModerated` | boolean |  |
| `data.fields.sellerPhone[].value` | string |  |
| `data.fields.sellerPhone[].verificationStatus` | string |  |
| `data.fields.subtotal[].bbox[]` | number |  |
| `data.fields.subtotal[].confidence` | number |  |
| `data.fields.subtotal[].fieldDataId` | string |  |
| `data.fields.subtotal[].isModerated` | boolean |  |
| `data.fields.subtotal[].value` | string |  |
| `data.fields.subtotal[].verificationStatus` | string |  |
| `data.fields.totalTax[].bbox[]` | number |  |
| `data.fields.totalTax[].confidence` | number |  |
| `data.fields.totalTax[].fieldDataId` | string |  |
| `data.fields.totalTax[].isModerated` | boolean |  |
| `data.fields.totalTax[].value` | string |  |
| `data.fields.totalTax[].verificationStatus` | string |  |
| `data.fields.totalTax%[].bbox[]` | number |  |
| `data.fields.totalTax%[].confidence` | number |  |
| `data.fields.totalTax%[].fieldDataId` | string |  |
| `data.fields.totalTax%[].isModerated` | boolean |  |
| `data.fields.totalTax%[].value` | string |  |
| `data.fields.totalTax%[].verificationStatus` | string |  |
| `data.tables[].bbox[]` | number |  |
| `data.tables[].cells[].bbox[]` | number |  |
| `data.tables[].cells[].cellId` | string |  |
| `data.tables[].cells[].col` | number |  |
| `data.tables[].cells[].header` | string |  |
| `data.tables[].cells[].isModerated` | boolean |  |
| `data.tables[].cells[].row` | number |  |
| `data.tables[].cells[].text` | string |  |
| `data.tables[].cells[].verificationStatus` | string |  |
| `data.tables[].tableId` | string |  |
| `imageUrl` | string |  |
| `pageId` | string |  |
| `pageNumber` | number |  |

## Native endpoint

Through the native Nanonets OCR API, this operation is `GET /workflows/:workflow_id/documents/:document_id/pages/:page_id` (base URL `https://app.nanonets.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-data.md) for the provider-specific parameters and requirements.

