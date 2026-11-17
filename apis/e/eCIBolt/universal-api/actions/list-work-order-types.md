# ECI Bolt: List Work Order Types



```
GET https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-work-order-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECI Bolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-work-order-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-work-order-types?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `refreshToken` | string | no | Token used to get the changed work_order_types, returned on the last page of the work_order_types. You should only send the refresh_token or the next_batch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "autoConfirm": {
        "checklist": "string",
        "cutoff": 1,
        "days": 1,
        "enabled": true,
        "reschedule": 1,
        "resend": 1,
        "time": "string"
      },
      "autoSendConirmationEmail": true,
      "billingContractTypeIds": [
        1
      ],
      "billingContractTypes": [
        "string"
      ],
      "completedEmail": {
        "enabled": true,
        "message": "ava@example.com"
      },
      "customField1": "string",
      "departmentType": "string",
      "departmentTypeId": 1,
      "deviceDisplay": true,
      "displayOrder": 1,
      "etag": "string",
      "forecastOrder": 1,
      "id": 1,
      "name": "Ava Chen",
      "officeIds": [
        "string"
      ],
      "offices": [
        "string"
      ],
      "printingOptions": {
        "customerNotes": "string",
        "jobStatuses": "string",
        "laborPay": "string",
        "options": "string",
        "statuses": "string",
        "timeAndLabor": "string"
      },
      "recurringWorkorder": true,
      "secondaryService": true,
      "standardBilling": true,
      "workType": "string",
      "workTypeId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `autoConfirm` | object |  |
| `autoConfirm.checklist` | string |  |
| `autoConfirm.cutoff` | number |  |
| `autoConfirm.days` | number |  |
| `autoConfirm.enabled` | boolean |  |
| `autoConfirm.reschedule` | number |  |
| `autoConfirm.resend` | number |  |
| `autoConfirm.time` | string |  |
| `autoSendConirmationEmail` | boolean |  |
| `billingContractTypeIds` | array<number> |  |
| `billingContractTypes` | array<string> |  |
| `completedEmail` | object |  |
| `completedEmail.enabled` | boolean |  |
| `completedEmail.message` | string |  |
| `customField1` | string |  |
| `departmentType` | string |  |
| `departmentTypeId` | number |  |
| `deviceDisplay` | boolean |  |
| `displayOrder` | number |  |
| `etag` | string |  |
| `forecastOrder` | number |  |
| `id` | number |  |
| `name` | string |  |
| `officeIds` | array |  |
| `offices` | array<string> |  |
| `printingOptions` | object | Map of printing option flags. Each key must be "0" or "1". |
| `printingOptions.customerNotes` | string |  |
| `printingOptions.jobStatuses` | string |  |
| `printingOptions.laborPay` | string |  |
| `printingOptions.options` | string |  |
| `printingOptions.statuses` | string |  |
| `printingOptions.timeAndLabor` | string |  |
| `recurringWorkorder` | boolean |  |
| `secondaryService` | boolean |  |
| `standardBilling` | boolean |  |
| `workType` | string |  |
| `workTypeId` | number |  |

## Native endpoint

Through the native ECI Bolt API, this operation is `GET /open/v1/work_order_types` (base URL `https://app.bolttech.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-work-order-types.md) for the provider-specific parameters and requirements.

