# Fatture in Cloud: Get Company Info

Retrieves company info from Fatture in Cloud.

```
GET https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/get-company-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fatture in Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/get-company-info?connectionId=$CONNECTION_ID&companyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/get-company-info?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessInfo": {
        "permissions": {
          "dicEmployees": "string",
          "dicSettings": "string",
          "dicTimesheet": "string",
          "ficArchive": "string",
          "ficCalendar": "string",
          "ficCashbook": "string",
          "ficClients": "string",
          "ficEmails": "ava@example.com",
          "ficExport": "string",
          "ficImportBankstatements": "string",
          "ficImportClientsSuppliers": "string",
          "ficImportIssuedDocuments": "string",
          "ficImportMultidata": "string",
          "ficImportProducts": "string",
          "ficInvoiceTrading": "string",
          "ficIssuedDocuments": "string",
          "ficIssuedDocumentsDetailed": {
            "creditNotes": "string",
            "deliveryNotes": "string",
            "invoices": "string",
            "orders": "string",
            "proformas": "string",
            "quotes": "string",
            "receipts": "string",
            "selfInvoices": "string",
            "supplierOrders": "string",
            "workReports": "string"
          },
          "ficProducts": "string",
          "ficReceipts": "string",
          "ficReceivedDocuments": "string",
          "ficRecurring": "string",
          "ficRiba": "string",
          "ficSettings": "string",
          "ficSituation": "string",
          "ficStock": "string",
          "ficSuppliers": "string",
          "ficTaxes": "string"
        },
        "role": "string",
        "throughAccountant": true
      },
      "canUseCoupon": true,
      "companyTsData": {
        "companyRegistryItemId": "string",
        "status": "string",
        "workspaceAttributeId": "string",
        "workspaceId": "string"
      },
      "dic": true,
      "dicPaymentSubject": "string",
      "dicPlanName": "Ava Chen",
      "email": "ava@example.com",
      "fic": true,
      "ficLicenseExpire": "2026-05-07T12:00:00.000Z",
      "ficNeedSetup": true,
      "ficPaymentSubject": "string",
      "ficPlanName": "Ava Chen",
      "ficSignupDate": "2026-05-07T12:00:00.000Z",
      "gracePeriod": true,
      "hasAutomaticRenewal": true,
      "id": 1,
      "isAccountant": true,
      "isAgyoActive": true,
      "name": "Ava Chen",
      "planInfo": {
        "functions": {
          "aiReconciliation": true,
          "archive": true,
          "attachPdfToXml": true,
          "cerved": true,
          "copilot": true,
          "documentAttachments": true,
          "eInvoice": true,
          "genius": true,
          "mailTracking": true,
          "paymentNotifications": true,
          "priceLists": true,
          "receipts": true,
          "recurring": true,
          "smtp": true,
          "sofort": true,
          "stock": true,
          "subaccounts": true,
          "tesseraSanitaria": true,
          "tsAgent": true,
          "tsDigital": true,
          "tsPay": true
        },
        "functionsStatus": {
          "tsDigital": {
            "active": true
          },
          "tsPay": {
            "active": true
          }
        },
        "limits": {
          "clients": 1,
          "documents": 1,
          "products": 1,
          "suppliers": 1
        }
      },
      "registrationService": "string",
      "retryMode": {
        "enabled": true
      },
      "type": "string",
      "useDic": true,
      "useFic": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessInfo.permissions.dicEmployees` | string |  |
| `accessInfo.permissions.dicSettings` | string |  |
| `accessInfo.permissions.dicTimesheet` | string |  |
| `accessInfo.permissions.ficArchive` | string |  |
| `accessInfo.permissions.ficCalendar` | string |  |
| `accessInfo.permissions.ficCashbook` | string |  |
| `accessInfo.permissions.ficClients` | string |  |
| `accessInfo.permissions.ficEmails` | string |  |
| `accessInfo.permissions.ficExport` | string |  |
| `accessInfo.permissions.ficImportBankstatements` | string |  |
| `accessInfo.permissions.ficImportClientsSuppliers` | string |  |
| `accessInfo.permissions.ficImportIssuedDocuments` | string |  |
| `accessInfo.permissions.ficImportMultidata` | string |  |
| `accessInfo.permissions.ficImportProducts` | string |  |
| `accessInfo.permissions.ficInvoiceTrading` | string |  |
| `accessInfo.permissions.ficIssuedDocuments` | string |  |
| `accessInfo.permissions.ficIssuedDocumentsDetailed.creditNotes` | string |  |
| `accessInfo.permissions.ficIssuedDocumentsDetailed.deliveryNotes` | string |  |
| `accessInfo.permissions.ficIssuedDocumentsDetailed.invoices` | string |  |
| `accessInfo.permissions.ficIssuedDocumentsDetailed.orders` | string |  |
| `accessInfo.permissions.ficIssuedDocumentsDetailed.proformas` | string |  |
| `accessInfo.permissions.ficIssuedDocumentsDetailed.quotes` | string |  |
| `accessInfo.permissions.ficIssuedDocumentsDetailed.receipts` | string |  |
| `accessInfo.permissions.ficIssuedDocumentsDetailed.selfInvoices` | string |  |
| `accessInfo.permissions.ficIssuedDocumentsDetailed.supplierOrders` | string |  |
| `accessInfo.permissions.ficIssuedDocumentsDetailed.workReports` | string |  |
| `accessInfo.permissions.ficProducts` | string |  |
| `accessInfo.permissions.ficReceipts` | string |  |
| `accessInfo.permissions.ficReceivedDocuments` | string |  |
| `accessInfo.permissions.ficRecurring` | string |  |
| `accessInfo.permissions.ficRiba` | string |  |
| `accessInfo.permissions.ficSettings` | string |  |
| `accessInfo.permissions.ficSituation` | string |  |
| `accessInfo.permissions.ficStock` | string |  |
| `accessInfo.permissions.ficSuppliers` | string |  |
| `accessInfo.permissions.ficTaxes` | string |  |
| `accessInfo.role` | string |  |
| `accessInfo.throughAccountant` | boolean |  |
| `canUseCoupon` | boolean |  |
| `companyTsData.companyRegistryItemId` | string |  |
| `companyTsData.status` | string |  |
| `companyTsData.workspaceAttributeId` | string |  |
| `companyTsData.workspaceId` | string |  |
| `dic` | boolean |  |
| `dicPaymentSubject` | string |  |
| `dicPlanName` | string |  |
| `email` | string |  |
| `fic` | boolean |  |
| `ficLicenseExpire` | date |  |
| `ficNeedSetup` | boolean |  |
| `ficPaymentSubject` | string |  |
| `ficPlanName` | string |  |
| `ficSignupDate` | date |  |
| `gracePeriod` | boolean |  |
| `hasAutomaticRenewal` | boolean |  |
| `id` | number |  |
| `isAccountant` | boolean |  |
| `isAgyoActive` | boolean |  |
| `name` | string |  |
| `planInfo.functions.aiReconciliation` | boolean |  |
| `planInfo.functions.archive` | boolean |  |
| `planInfo.functions.attachPdfToXml` | boolean |  |
| `planInfo.functions.cerved` | boolean |  |
| `planInfo.functions.copilot` | boolean |  |
| `planInfo.functions.documentAttachments` | boolean |  |
| `planInfo.functions.eInvoice` | boolean |  |
| `planInfo.functions.genius` | boolean |  |
| `planInfo.functions.mailTracking` | boolean |  |
| `planInfo.functions.paymentNotifications` | boolean |  |
| `planInfo.functions.priceLists` | boolean |  |
| `planInfo.functions.receipts` | boolean |  |
| `planInfo.functions.recurring` | boolean |  |
| `planInfo.functions.smtp` | boolean |  |
| `planInfo.functions.sofort` | boolean |  |
| `planInfo.functions.stock` | boolean |  |
| `planInfo.functions.subaccounts` | boolean |  |
| `planInfo.functions.tesseraSanitaria` | boolean |  |
| `planInfo.functions.tsAgent` | boolean |  |
| `planInfo.functions.tsDigital` | boolean |  |
| `planInfo.functions.tsPay` | boolean |  |
| `planInfo.functionsStatus.tsDigital.active` | boolean |  |
| `planInfo.functionsStatus.tsPay.active` | boolean |  |
| `planInfo.limits.clients` | number |  |
| `planInfo.limits.documents` | number |  |
| `planInfo.limits.products` | number |  |
| `planInfo.limits.suppliers` | number |  |
| `registrationService` | string |  |
| `retryMode.enabled` | boolean |  |
| `type` | string |  |
| `useDic` | boolean |  |
| `useFic` | boolean |  |

## Native endpoint

Through the native Fatture in Cloud API, this operation is `GET /c/:company_id/company/info` (base URL `https://api-v2.fattureincloud.it`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-info.md) for the provider-specific parameters and requirements.

