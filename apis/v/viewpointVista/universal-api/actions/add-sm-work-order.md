# Viewpoint Vista: Add SM Work Order

Adds a Service Management work order header and automatically creates default Scope 1 in SMWorkOrderScope.

```
POST https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-sm-work-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-sm-work-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sMCo": 1,
  "serviceCenter": "string",
  "customer": 1,
  "workOrderType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-sm-work-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sMCo": 1,
    "serviceCenter": "string",
    "customer": 1,
    "workOrderType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sMCo` | number | yes |  |
| `serviceCenter` | string | yes | Enter the Service center that this request is assigned to. |
| `customer` | number | yes | The SM Customer for this order. **Required when `WorkOrderType` is `C-Customer`. |
| `job` | string | no | The JC Job for this work order. Required when `WorkOrderType` is `J-Job`. |
| `jcco` | number | no | Enter JC Company. Required when `WorkOrderType` is `J-Job` |
| `custGroup` | number | no |  |
| `servicesite` | string | no | Enter a Site ID. |
| `workOrderType` | string | yes |  |
| `workOrderQuote` | string | no |  |
| `wostatus` | number | no |  |
| `contactname` | string | no | Enter the contact name. |
| `contactphone` | string | no | Enter the contact phone. |
| `description` | string | no | Enter a description of the request. |
| `notes` | string | no | Enter a note about this work order. |
| `isnew` | boolean | no |  |
| `craftTemplate` | number | no | Enter a template code to identify craft/class pay rates. |
| `costingmethod` | list<string> | no | Select a costing method. |
| `leadtechnician` | string | no | Enter the lead technician. |
| `reviewer` | string | no | Enter the Reviewer for this work. |
| `prstate` | string | no | Enter the State Code that identifies the location that work will be performed. |
| `prlocalcode` | string | no | Enter the Payroll Local Code. |
| `uniqueattchid` | string | no |  |
| `requestedby` | string | no | Enter the name of the person making this request. |
| `requestedbyphone` | string | no | Enter the phone number of the person making this request. |
| `requesteddate` | string | no | Enter the date that the request was made. Format: `YYYY-MM-DD` |
| `requestedtime` | string | no | Enter the time that the request was made. Format: `HH:mm` |
| `certified` | list<string> | no | Certified Payroll. For customer work orders only. Options: - `Y`-Yes - `N`-No. |
| `certifiedStartDate` | string | no | Enter the start date for certifieds. Format: YYYY-MM-DD. |
| `enteredby` | string | no | The user that entered the work order. |
| `entereddatetime` | string | no | The date the work order was entered. Format: `YYYY-MM-DD HH:mm` |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/actions/add` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-sm-work-order.md) for the provider-specific parameters and requirements.

