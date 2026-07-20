# Zoho FSM: Create Work Order

Creates a new work order in Zoho FSM.

```
POST https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-work-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho FSM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-work-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-work-order', {
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
| `data[].adjustment` | string | no |  |
| `data[].asset` | string | no |  |
| `data[].billing_address.id` | string | no |  |
| `data[].company` | string | no |  |
| `data[].contact` | string | no |  |
| `data[].currency` | string | no |  |
| `data[].exchange_rate` | number | no |  |
| `data[].grand_total` | number | no |  |
| `data[].record_template` | string | no |  |
| `data[].service_address.id` | string | no |  |
| `data[].service_line_items[].amount` | number | no |  |
| `data[].service_line_items[].contact` | string | no |  |
| `data[].service_line_items[].description` | string | no |  |
| `data[].service_line_items[].discount` | string | no |  |
| `data[].service_line_items[].discount_type` | string | no |  |
| `data[].service_line_items[].line_item_amount` | number | no |  |
| `data[].service_line_items[].list_price` | number | no |  |
| `data[].service_line_items[].part_line_items[].part` | string | no |  |
| `data[].service_line_items[].part_line_items[].quantity` | number | no |  |
| `data[].service_line_items[].part_line_items[].sequence` | number | no |  |
| `data[].service_line_items[].quantity` | number | no |  |
| `data[].service_line_items[].sequence` | number | no |  |
| `data[].service_line_items[].service` | string | no |  |
| `data[].service_line_items[].service_tasks_line_items[].sequence` | number | no |  |
| `data[].service_line_items[].service_tasks_line_items[].service_task` | string | no |  |
| `data[].service_line_items[].service_tasks_line_items[].service_task_name` | string | no |  |
| `data[].service_line_items[].status` | string | no |  |
| `data[].service_line_items[].tax.tax_exemption_code` | string | no |  |
| `data[].service_line_items[].tax.tax_exemption_id` | string | no |  |
| `data[].service_line_items[].tax.tax_id` | string | no |  |
| `data[].service_line_items[].tax.tax_name` | string | no |  |
| `data[].service_line_items[].tax.tax_percentage` | string | no |  |
| `data[].service_line_items[].unit` | string | no |  |
| `data[].sub_total` | number | no |  |
| `data[].summary` | string | no |  |
| `data[].tax_amount` | string | no |  |
| `data[].territory` | string | no |  |
| `data[].type` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "data": {
        "serviceLineItems": [
          {
            "createdBy": {
              "id": "string",
              "name": "Ava Chen"
            },
            "createdTime": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "modifiedBy": {
              "id": "string",
              "name": "Ava Chen"
            },
            "modifiedTime": "2026-05-07T12:00:00.000Z",
            "tabName": "Ava Chen",
            "uid": "string"
          }
        ],
        "serviceTasksLineItems": [
          {
            "createdBy": {
              "id": "string",
              "name": "Ava Chen"
            },
            "createdTime": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "modifiedBy": {
              "id": "string",
              "name": "Ava Chen"
            },
            "modifiedTime": "2026-05-07T12:00:00.000Z",
            "tabName": "Ava Chen",
            "uid": "string"
          }
        ],
        "workOrders": [
          {
            "createdBy": {
              "id": "string",
              "name": "Ava Chen"
            },
            "createdTime": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "modifiedBy": {
              "id": "string",
              "name": "Ava Chen"
            },
            "modifiedTime": "2026-05-07T12:00:00.000Z",
            "tabName": "Ava Chen",
            "uid": "string"
          }
        ]
      },
      "result": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `data.serviceLineItems[].createdBy.id` | string |  |
| `data.serviceLineItems[].createdBy.name` | string |  |
| `data.serviceLineItems[].createdTime` | date |  |
| `data.serviceLineItems[].id` | string |  |
| `data.serviceLineItems[].modifiedBy.id` | string |  |
| `data.serviceLineItems[].modifiedBy.name` | string |  |
| `data.serviceLineItems[].modifiedTime` | date |  |
| `data.serviceLineItems[].tabName` | string |  |
| `data.serviceLineItems[].uid` | string |  |
| `data.serviceTasksLineItems[].createdBy.id` | string |  |
| `data.serviceTasksLineItems[].createdBy.name` | string |  |
| `data.serviceTasksLineItems[].createdTime` | date |  |
| `data.serviceTasksLineItems[].id` | string |  |
| `data.serviceTasksLineItems[].modifiedBy.id` | string |  |
| `data.serviceTasksLineItems[].modifiedBy.name` | string |  |
| `data.serviceTasksLineItems[].modifiedTime` | date |  |
| `data.serviceTasksLineItems[].tabName` | string |  |
| `data.serviceTasksLineItems[].uid` | string |  |
| `data.workOrders[].createdBy.id` | string |  |
| `data.workOrders[].createdBy.name` | string |  |
| `data.workOrders[].createdTime` | date |  |
| `data.workOrders[].id` | string |  |
| `data.workOrders[].modifiedBy.id` | string |  |
| `data.workOrders[].modifiedBy.name` | string |  |
| `data.workOrders[].modifiedTime` | date |  |
| `data.workOrders[].tabName` | string |  |
| `data.workOrders[].uid` | string |  |
| `result` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho FSM API, this operation is `POST /Work_Orders` (base URL `{{credentials.accessTokenRequest.api_domain}}/fsm/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-work-order.md) for the provider-specific parameters and requirements.

