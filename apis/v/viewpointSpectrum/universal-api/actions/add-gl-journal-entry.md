# Viewpoint Spectrum: Add G/L Journal Entry

Adds one line to a G/L journal entry batch in Spectrum. Lines sent with the same GUID form one balanced journal.

```
POST https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/add-gl-journal-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Spectrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/add-gl-journal-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionDate": "2026-10-31",
  "journalDesc": "string",
  "journalRemarks": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/add-gl-journal-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactionDate": "2026-10-31",
    "journalDesc": "string",
    "journalRemarks": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `guid` | string | no | Use the same GUID on every line of one journal, and a new GUID for the next journal. Spectrum generates one when blank. Example: `550e8400-e29b-41d4-a716-446655440000`. |
| `transactionDate` | string | yes | Calendar date as YYYY-MM-DD (or MM/DD/YYYY). Must be within the current G/L processing dates. The first line sets the journal header date. Example: `2026-10-31`. |
| `journalDesc` | string | yes | The first record determines the description for the journal header. |
| `journalRemarks` | string | yes | The first record determines the remarks for the journal header. |
| `glAccount` | string | no | Enter the G/L account without dashes. |
| `glDebitAmount` | number | no | Positive values only. The complete journal batch must balance. |
| `glCreditAmount` | number | no | Positive values only. The complete journal batch must balance. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyCode` | string | no | Spectrum company for this journal. Defaults to the connection's company. Every line of one journal must use the same company. |
| `costCenter` | string | no | For cost center companies, required on the first record for the header and on non-direct G/L account lines. |
| `lineReference` | string | no |  |
| `jobNumber` | string | no | Required for direct job cost accounts. |
| `phaseCode` | string | no | Enter the phase code without dashes. Required with Job Number and Cost Type for direct job cost accounts. |
| `costType` | string | no | Required for direct job cost accounts. |
| `equipmentCode` | string | no | Required for direct equipment cost accounts. |
| `equipmentCostCategory` | string | no | Required for direct equipment cost accounts. |
| `equipmentWorkOrder` | string | no | Required, optional, or disallowed according to the equipment cost category data entry rule. |
| `woNumber` | string | no | Required for direct work order cost accounts. The work order must not be complete. |
| `woEquipment` | string | no | Required when the work order installation requires equipment for work order transactions. |
| `woComponent` | string | no | Required when the installation requires components and the selected equipment has components. |
| `woContract` | string | no |  |
| `woSellprice` | number | no |  |
| `currentRecordNumber` | string | no | Defined in AddGLTrans.jws but omitted from the help page. Confirm numbering with your Spectrum developer before batch testing. |
| `totalRecordCount` | string | no | Defined in AddGLTrans.jws but omitted from the help page. Confirm batch usage with your Spectrum developer. |
| `isBatchFlag` | string | no | Defined as a string in AddGLTrans.jws. Accepted values are not documented on the help page; confirm them before batch testing. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Spectrum API returns.

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `POST ws/AddGLTrans` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-gl-journal-entry.md) for the provider-specific parameters and requirements.

