# Viewpoint Spectrum: Send Timesheet (SOAP)



```
POST https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/send-timesheet-soap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Spectrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/send-timesheet-soap" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/send-timesheet-soap', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batchCode` | string | no | Discount percent. |
| `employeeCode` | string | no | Insurance certificate flag (Y/N). |
| `timeCardDate` | string | no | On hold flag (Y/N). |
| `department` | string | no | Default G/L Code. |
| `spectrumJob` | string | no | 1099 flag (Y/N). |
| `phase` | string | no | Alternate 1099 name. |
| `costType` | string | no | 1099 payment indicator. |
| `payType` | string | no | Social Security number. |
| `hours` | string | no | Federal ID number. |
| `wageCode` | string | no | Vendor email. |
| `costCenter` | string | no | Contact phone. |
| `equipmentCode` | string | no |  |
| `woNumber` | string | no |  |
| `woEquipment` | string | no |  |
| `woComponent` | string | no |  |
| `sCContract` | string | no |  |
| `pmWorkOrder` | string | no |  |
| `pmEquipment` | string | no |  |
| `pmAssembly` | string | no |  |
| `pmComponent` | string | no |  |
| `shiftCode` | string | no |  |
| `workLocality` | string | no |  |
| `notes` | string | no |  |
| `unionCode` | string | no |  |
| `classCode` | string | no |  |
| `tradeCode` | string | no |  |
| `taxLocality` | string | no |  |
| `taxState` | string | no |  |
| `workerCompCode` | string | no |  |
| `workCounty` | string | no |  |
| `locality` | string | no |  |
| `state` | string | no |  |
| `hoursEmployee` | string | no |  |
| `message` | string | no |  |
| `interCompanyCode` | string | no |  |
| `additionalJTDQuantity` | string | no |  |
| `workDate` | string | no |  |
| `payRateCode` | string | no |  |
| `crewNumber` | string | no |  |
| `costCategoryCode` | string | no |  |
| `payRate` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Spectrum API returns.

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `POST ws/PreTimeCard` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-timesheet-soap.md) for the provider-specific parameters and requirements.

