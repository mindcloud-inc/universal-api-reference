# Rillion Prime: Create Invoice Diary Post



```
POST https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-invoice-diary-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-invoice-diary-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceDiary": {},
  "invoiceDiaryHeadersOnly": 1,
  "invoiceDiaryForProcessing": true,
  "invoiceDiaryLocked": true,
  "invoiceDiaryLockedRowId": 1,
  "invoiceDiaryLockedRowLoginName": "Ava Chen",
  "invoiceDiaryLockedRowRole": "string",
  "invoiceDiaryRowState": 1,
  "invoiceDiarySelected": true,
  "invoiceDiaryKeyValuesRowState": 1,
  "invoiceDiaryInvoiceDiaryId": 1,
  "invoiceDiaryInvoiceId": 1,
  "invoiceDiaryType": 1,
  "invoiceDiaryInvestigateType": 1,
  "invoiceDiaryCreateTime": "2026-05-07T12:00:00.000Z",
  "invoiceDiaryCreateUser": "string",
  "invoiceDiaryCreateRole": "string",
  "invoiceDiaryInvestigateRole": "string",
  "invoiceDiaryNote": "string",
  "invoiceDiaryAttachedFile": "string",
  "invoiceDiaryVisibleInSupplierPortal": true,
  "invoiceDiaryCreateUserFullName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-invoice-diary-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceDiary": {},
    "invoiceDiaryHeadersOnly": 1,
    "invoiceDiaryForProcessing": true,
    "invoiceDiaryLocked": true,
    "invoiceDiaryLockedRowId": 1,
    "invoiceDiaryLockedRowLoginName": "Ava Chen",
    "invoiceDiaryLockedRowRole": "string",
    "invoiceDiaryRowState": 1,
    "invoiceDiarySelected": true,
    "invoiceDiaryKeyValuesRowState": 1,
    "invoiceDiaryInvoiceDiaryId": 1,
    "invoiceDiaryInvoiceId": 1,
    "invoiceDiaryType": 1,
    "invoiceDiaryInvestigateType": 1,
    "invoiceDiaryCreateTime": "2026-05-07T12:00:00.000Z",
    "invoiceDiaryCreateUser": "string",
    "invoiceDiaryCreateRole": "string",
    "invoiceDiaryInvestigateRole": "string",
    "invoiceDiaryNote": "string",
    "invoiceDiaryAttachedFile": "string",
    "invoiceDiaryVisibleInSupplierPortal": true,
    "invoiceDiaryCreateUserFullName": "Ava Chen",
    "invoiceDiary": {},
    "invoiceDiaryHeadersOnly": 1,
    "invoiceDiaryForProcessing": true,
    "invoiceDiaryLocked": true,
    "invoiceDiaryLockedRowId": 1,
    "invoiceDiaryLockedRowLoginName": "Ava Chen",
    "invoiceDiaryLockedRowRole": "string",
    "invoiceDiaryRowState": 1,
    "invoiceDiarySelected": true,
    "invoiceDiaryKeyValuesRowState": 1,
    "invoiceDiaryInvoiceDiaryId": 1,
    "invoiceDiaryInvoiceId": 1,
    "invoiceDiaryType": 1,
    "invoiceDiaryInvestigateType": 1,
    "invoiceDiaryCreateTime": "2026-05-07T12:00:00.000Z",
    "invoiceDiaryCreateUser": "string",
    "invoiceDiaryCreateRole": "string",
    "invoiceDiaryInvestigateRole": "string",
    "invoiceDiaryNote": "string",
    "invoiceDiaryAttachedFile": "string",
    "invoiceDiaryVisibleInSupplierPortal": true,
    "invoiceDiaryCreateUserFullName": "Ava Chen",
    "invoiceDiary": {},
    "invoiceDiaryHeadersOnly": 1,
    "invoiceDiaryForProcessing": true,
    "invoiceDiaryLocked": true,
    "invoiceDiaryLockedRowId": 1,
    "invoiceDiaryLockedRowLoginName": "Ava Chen",
    "invoiceDiaryLockedRowRole": "string",
    "invoiceDiaryRowState": 1,
    "invoiceDiarySelected": true,
    "invoiceDiaryKeyValuesRowState": 1,
    "invoiceDiaryInvoiceDiaryId": 1,
    "invoiceDiaryInvoiceId": 1,
    "invoiceDiaryType": 1,
    "invoiceDiaryInvestigateType": 1,
    "invoiceDiaryCreateTime": "2026-05-07T12:00:00.000Z",
    "invoiceDiaryCreateUser": "string",
    "invoiceDiaryCreateRole": "string",
    "invoiceDiaryInvestigateRole": "string",
    "invoiceDiaryNote": "string",
    "invoiceDiaryAttachedFile": "string",
    "invoiceDiaryVisibleInSupplierPortal": true,
    "invoiceDiaryCreateUserFullName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceDiary` | object | yes | Request body value for InvoiceDiary. |
| `invoiceDiaryHeadersOnly` | number | yes | Request body value for InvoiceDiary HeadersOnly. |
| `invoiceDiaryForProcessing` | boolean | yes | Request body value for InvoiceDiary ForProcessing. |
| `invoiceDiaryLocked` | boolean | yes | Request body value for InvoiceDiary Locked. |
| `invoiceDiaryLockedRowId` | number | yes | Request body value for InvoiceDiary LockedRowId. |
| `invoiceDiaryLockedRowLoginName` | string | yes | Request body value for InvoiceDiary LockedRowLoginName. |
| `invoiceDiaryLockedRowRole` | string | yes | Request body value for InvoiceDiary LockedRowRole. |
| `invoiceDiaryRowState` | number | yes | Request body value for InvoiceDiary RowState. |
| `invoiceDiarySelected` | boolean | yes | Request body value for InvoiceDiary Selected. |
| `invoiceDiaryKeyValuesRowState` | number | yes | Request body value for InvoiceDiary KeyValuesRowState. |
| `invoiceDiaryInvoiceDiaryId` | number | yes | Request body value for InvoiceDiary InvoiceDiaryId. |
| `invoiceDiaryInvoiceId` | number | yes | Request body value for InvoiceDiary InvoiceId. |
| `invoiceDiaryType` | number | yes | Request body value for InvoiceDiary Type. |
| `invoiceDiaryInvestigateType` | number | yes | Request body value for InvoiceDiary InvestigateType. |
| `invoiceDiaryCreateTime` | date | yes | Request body value for InvoiceDiary CreateTime. |
| `invoiceDiaryCreateUser` | string | yes | Request body value for InvoiceDiary CreateUser. |
| `invoiceDiaryCreateRole` | string | yes | Request body value for InvoiceDiary CreateRole. |
| `invoiceDiaryInvestigateRole` | string | yes | Request body value for InvoiceDiary InvestigateRole. |
| `invoiceDiaryNote` | string | yes | Request body value for InvoiceDiary Note. |
| `invoiceDiaryAttachedFile` | string | yes | Request body value for InvoiceDiary AttachedFile. |
| `invoiceDiaryVisibleInSupplierPortal` | boolean | yes | Request body value for InvoiceDiary VisibleInSupplierPortal. |
| `invoiceDiaryCreateUserFullName` | string | yes | Request body value for InvoiceDiary CreateUserFullName. |
| `invoiceDiary` | object | yes | Request body value for InvoiceDiary. |
| `invoiceDiaryHeadersOnly` | number | yes | Request body value for InvoiceDiary HeadersOnly. |
| `invoiceDiaryForProcessing` | boolean | yes | Request body value for InvoiceDiary ForProcessing. |
| `invoiceDiaryLocked` | boolean | yes | Request body value for InvoiceDiary Locked. |
| `invoiceDiaryLockedRowId` | number | yes | Request body value for InvoiceDiary LockedRowId. |
| `invoiceDiaryLockedRowLoginName` | string | yes | Request body value for InvoiceDiary LockedRowLoginName. |
| `invoiceDiaryLockedRowRole` | string | yes | Request body value for InvoiceDiary LockedRowRole. |
| `invoiceDiaryRowState` | number | yes | Request body value for InvoiceDiary RowState. |
| `invoiceDiarySelected` | boolean | yes | Request body value for InvoiceDiary Selected. |
| `invoiceDiaryKeyValuesRowState` | number | yes | Request body value for InvoiceDiary KeyValuesRowState. |
| `invoiceDiaryInvoiceDiaryId` | number | yes | Request body value for InvoiceDiary InvoiceDiaryId. |
| `invoiceDiaryInvoiceId` | number | yes | Request body value for InvoiceDiary InvoiceId. |
| `invoiceDiaryType` | number | yes | Request body value for InvoiceDiary Type. |
| `invoiceDiaryInvestigateType` | number | yes | Request body value for InvoiceDiary InvestigateType. |
| `invoiceDiaryCreateTime` | date | yes | Request body value for InvoiceDiary CreateTime. |
| `invoiceDiaryCreateUser` | string | yes | Request body value for InvoiceDiary CreateUser. |
| `invoiceDiaryCreateRole` | string | yes | Request body value for InvoiceDiary CreateRole. |
| `invoiceDiaryInvestigateRole` | string | yes | Request body value for InvoiceDiary InvestigateRole. |
| `invoiceDiaryNote` | string | yes | Request body value for InvoiceDiary Note. |
| `invoiceDiaryAttachedFile` | string | yes | Request body value for InvoiceDiary AttachedFile. |
| `invoiceDiaryVisibleInSupplierPortal` | boolean | yes | Request body value for InvoiceDiary VisibleInSupplierPortal. |
| `invoiceDiaryCreateUserFullName` | string | yes | Request body value for InvoiceDiary CreateUserFullName. |
| `invoiceDiary` | object | yes | Request body value for InvoiceDiary. |
| `invoiceDiaryHeadersOnly` | number | yes | Request body value for InvoiceDiary HeadersOnly. |
| `invoiceDiaryForProcessing` | boolean | yes | Request body value for InvoiceDiary ForProcessing. |
| `invoiceDiaryLocked` | boolean | yes | Request body value for InvoiceDiary Locked. |
| `invoiceDiaryLockedRowId` | number | yes | Request body value for InvoiceDiary LockedRowId. |
| `invoiceDiaryLockedRowLoginName` | string | yes | Request body value for InvoiceDiary LockedRowLoginName. |
| `invoiceDiaryLockedRowRole` | string | yes | Request body value for InvoiceDiary LockedRowRole. |
| `invoiceDiaryRowState` | number | yes | Request body value for InvoiceDiary RowState. |
| `invoiceDiarySelected` | boolean | yes | Request body value for InvoiceDiary Selected. |
| `invoiceDiaryKeyValuesRowState` | number | yes | Request body value for InvoiceDiary KeyValuesRowState. |
| `invoiceDiaryInvoiceDiaryId` | number | yes | Request body value for InvoiceDiary InvoiceDiaryId. |
| `invoiceDiaryInvoiceId` | number | yes | Request body value for InvoiceDiary InvoiceId. |
| `invoiceDiaryType` | number | yes | Request body value for InvoiceDiary Type. |
| `invoiceDiaryInvestigateType` | number | yes | Request body value for InvoiceDiary InvestigateType. |
| `invoiceDiaryCreateTime` | date | yes | Request body value for InvoiceDiary CreateTime. |
| `invoiceDiaryCreateUser` | string | yes | Request body value for InvoiceDiary CreateUser. |
| `invoiceDiaryCreateRole` | string | yes | Request body value for InvoiceDiary CreateRole. |
| `invoiceDiaryInvestigateRole` | string | yes | Request body value for InvoiceDiary InvestigateRole. |
| `invoiceDiaryNote` | string | yes | Request body value for InvoiceDiary Note. |
| `invoiceDiaryAttachedFile` | string | yes | Request body value for InvoiceDiary AttachedFile. |
| `invoiceDiaryVisibleInSupplierPortal` | boolean | yes | Request body value for InvoiceDiary VisibleInSupplierPortal. |
| `invoiceDiaryCreateUserFullName` | string | yes | Request body value for InvoiceDiary CreateUserFullName. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime API returns.

## Native endpoint

Through the native Rillion Prime API, this operation is `POST /invoice/diary` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice-diary-post.md) for the provider-specific parameters and requirements.

