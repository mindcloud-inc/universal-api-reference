# Create Bill Item with Sage Intacct

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://api.intacct.com/ia/xml/xmlgw.phtml`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/xml` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `apbillitems[].accountNo` | body | `string` | no |
| `apbillitems[].taxEntries[].detailId` | body | `string` | no |
| `whenCreated` | body | `string` | no |
| `apbillitems[].accountLabel` | body | `string` | no |
| `apbillitems[].taxEntries[].trx_tax` | body | `string` | no |
| `whenPosted` | body | `string` | no |
| `apbillitems[].offsetGlaAccountNo` | body | `string` | no |
| `vendorId` | body | `string` | no |
| `apbillitems[].trxAmount` | body | `string` | no |
| `recordId` | body | `string` | no |
| `apbillitems[].totalTrxAmount` | body | `string` | no |
| `docNumber` | body | `string` | no |
| `apbillitems[].entryDescription` | body | `string` | no |
| `description` | body | `string` | no |
| `apbillitems[].form1099` | body | `boolean` | no |
| `termName` | body | `string` | no |
| `apbillitems[].form1099Type` | body | `string` | no |
| `recPaymentDate` | body | `string` | no |
| `apbillitems[].form1099Box` | body | `string` | no |
| `supdocid` | body | `string` | no |
| `apbillitems[].billable` | body | `boolean` | no |
| `whenDue` | body | `string` | no |
| `apbillitems[].allocationId` | body | `string` | no |
| `paymentPriority` | body | `string` | no |
| `apbillitems[].departmentId` | body | `string` | no |
| `onHold` | body | `boolean` | no |
| `apbillitems[].projectId` | body | `string` | no |
| `currency` | body | `string` | no |
| `apbillitems[].taskId` | body | `string` | no |
| `baseCurr` | body | `string` | no |
| `apbillitems[]` | body | `array` | no |
| `apbillitems[].costTypeId` | body | `string` | no |
| `apbillitems[].customerId` | body | `string` | no |
| `apbillitems[].customerId` | body | `string` | no |
| `apbillitems[].vendorId` | body | `string` | no |
| `apbillitems[].employeeId` | body | `string` | no |
| `apbillitems[].itemId` | body | `string` | no |
| `apbillitems[].classId` | body | `string` | no |
| `apbillitems[].contractId` | body | `string` | no |
| `apbillitems[].warehouseId` | body | `string` | no |
| `apbillitems[].gldim*` | body | `number` | no |
| `apbillitems[].partialExempt` | body | `boolean` | no |
| `apbillitems[].taxEntries[]` | body | `array` | no |
| `apbillitems[].locationId` | body | `string` | no |
