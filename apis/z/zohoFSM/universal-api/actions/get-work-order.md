# Zoho FSM: Get Work Order

Retrieves work order details from Zoho FSM.

```
GET https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/get-work-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho FSM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/get-work-order?connectionId=$CONNECTION_ID&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/get-work-order?${params}`, {
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
| `recordId` | string | yes | The Zoho FSM record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$currencySymbol": "string",
      "$editable": true,
      "$inactive": true,
      "$permissions": {
        "delete": true,
        "edit": true,
        "read": true
      },
      "adjustment": 1,
      "billingAddress": {
        "billingCity": "string",
        "billingCountry": "string",
        "billingState": "string",
        "billingStreet1": "string",
        "billingZipCode": "string",
        "id": "string",
        "name": "Ava Chen"
      },
      "billingStatus": "string",
      "company": {
        "id": "string",
        "name": "Ava Chen"
      },
      "config": "string",
      "contact": {
        "id": "string",
        "name": "Ava Chen"
      },
      "createdBy": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "discountType": "string",
      "exchangeRate": 1,
      "grandTotal": 1,
      "id": "string",
      "location": "string",
      "modifiedBy": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "owner": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "roundOff": 1,
      "serviceAddress": {
        "id": "string",
        "name": "Ava Chen",
        "serviceCity": "string",
        "serviceCountry": "string",
        "serviceState": "string",
        "serviceStreet1": "string",
        "serviceZipCode": "string"
      },
      "serviceLineItems": [
        {
          "amount": 1,
          "billingStatus": "string",
          "contact": {
            "id": "string",
            "name": "Ava Chen"
          },
          "createdBy": {
            "email": "ava@example.com",
            "id": "string",
            "name": "Ava Chen"
          },
          "createdTime": "2026-05-07T12:00:00.000Z",
          "currency": "string",
          "customerPreference": 1,
          "discount": 1,
          "discountType": "string",
          "exchangeRate": 1,
          "id": "string",
          "isOptional": true,
          "lineItemAmount": 1,
          "listPrice": 1,
          "modifiedBy": {
            "email": "ava@example.com",
            "id": "string",
            "name": "Ava Chen"
          },
          "modifiedTime": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "owner": {
            "email": "ava@example.com",
            "id": "string",
            "name": "Ava Chen"
          },
          "quantity": 1,
          "quantitySource": "string",
          "sequence": 1,
          "service": {
            "id": "string",
            "name": "Ava Chen"
          },
          "status": "string",
          "unit": "string",
          "userPreference": true,
          "workOrder": {
            "id": "string",
            "name": "Ava Chen"
          }
        }
      ],
      "serviceTasksLineItems": [
        {
          "createdTime": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "modifiedTime": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "serviceLineItem": {
            "id": "string",
            "name": "Ava Chen",
            "service": "string"
          },
          "serviceTask": {
            "id": "string",
            "name": "Ava Chen"
          },
          "serviceTaskName": "Ava Chen",
          "status": "string",
          "workOrder": {
            "id": "string",
            "name": "Ava Chen"
          }
        }
      ],
      "status": "string",
      "subTotal": 1,
      "summary": "string",
      "taxAmount": 1,
      "territory": {
        "id": "string",
        "name": "Ava Chen"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$currencySymbol` | string |  |
| `$editable` | boolean |  |
| `$inactive` | boolean |  |
| `$permissions.delete` | boolean |  |
| `$permissions.edit` | boolean |  |
| `$permissions.read` | boolean |  |
| `adjustment` | number |  |
| `billingAddress.billingCity` | string |  |
| `billingAddress.billingCountry` | string |  |
| `billingAddress.billingState` | string |  |
| `billingAddress.billingStreet1` | string |  |
| `billingAddress.billingZipCode` | string |  |
| `billingAddress.id` | string |  |
| `billingAddress.name` | string |  |
| `billingStatus` | string |  |
| `company.id` | string |  |
| `company.name` | string |  |
| `config` | string |  |
| `contact.id` | string |  |
| `contact.name` | string |  |
| `createdBy.email` | string |  |
| `createdBy.id` | string |  |
| `createdBy.name` | string |  |
| `createdTime` | date |  |
| `currency` | string |  |
| `discountType` | string |  |
| `exchangeRate` | number |  |
| `grandTotal` | number |  |
| `id` | string |  |
| `location` | string |  |
| `modifiedBy.email` | string |  |
| `modifiedBy.id` | string |  |
| `modifiedBy.name` | string |  |
| `modifiedTime` | date |  |
| `name` | string |  |
| `owner.email` | string |  |
| `owner.id` | string |  |
| `owner.name` | string |  |
| `roundOff` | number |  |
| `serviceAddress.id` | string |  |
| `serviceAddress.name` | string |  |
| `serviceAddress.serviceCity` | string |  |
| `serviceAddress.serviceCountry` | string |  |
| `serviceAddress.serviceState` | string |  |
| `serviceAddress.serviceStreet1` | string |  |
| `serviceAddress.serviceZipCode` | string |  |
| `serviceLineItems[].amount` | number |  |
| `serviceLineItems[].billingStatus` | string |  |
| `serviceLineItems[].contact.id` | string |  |
| `serviceLineItems[].contact.name` | string |  |
| `serviceLineItems[].createdBy.email` | string |  |
| `serviceLineItems[].createdBy.id` | string |  |
| `serviceLineItems[].createdBy.name` | string |  |
| `serviceLineItems[].createdTime` | date |  |
| `serviceLineItems[].currency` | string |  |
| `serviceLineItems[].customerPreference` | number |  |
| `serviceLineItems[].discount` | number |  |
| `serviceLineItems[].discountType` | string |  |
| `serviceLineItems[].exchangeRate` | number |  |
| `serviceLineItems[].id` | string |  |
| `serviceLineItems[].isOptional` | boolean |  |
| `serviceLineItems[].lineItemAmount` | number |  |
| `serviceLineItems[].listPrice` | number |  |
| `serviceLineItems[].modifiedBy.email` | string |  |
| `serviceLineItems[].modifiedBy.id` | string |  |
| `serviceLineItems[].modifiedBy.name` | string |  |
| `serviceLineItems[].modifiedTime` | date |  |
| `serviceLineItems[].name` | string |  |
| `serviceLineItems[].owner.email` | string |  |
| `serviceLineItems[].owner.id` | string |  |
| `serviceLineItems[].owner.name` | string |  |
| `serviceLineItems[].quantity` | number |  |
| `serviceLineItems[].quantitySource` | string |  |
| `serviceLineItems[].sequence` | number |  |
| `serviceLineItems[].service.id` | string |  |
| `serviceLineItems[].service.name` | string |  |
| `serviceLineItems[].status` | string |  |
| `serviceLineItems[].unit` | string |  |
| `serviceLineItems[].userPreference` | boolean |  |
| `serviceLineItems[].workOrder.id` | string |  |
| `serviceLineItems[].workOrder.name` | string |  |
| `serviceTasksLineItems[].createdTime` | date |  |
| `serviceTasksLineItems[].id` | string |  |
| `serviceTasksLineItems[].modifiedTime` | date |  |
| `serviceTasksLineItems[].name` | string |  |
| `serviceTasksLineItems[].serviceLineItem.id` | string |  |
| `serviceTasksLineItems[].serviceLineItem.name` | string |  |
| `serviceTasksLineItems[].serviceLineItem.service` | string |  |
| `serviceTasksLineItems[].serviceTask.id` | string |  |
| `serviceTasksLineItems[].serviceTask.name` | string |  |
| `serviceTasksLineItems[].serviceTaskName` | string |  |
| `serviceTasksLineItems[].status` | string |  |
| `serviceTasksLineItems[].workOrder.id` | string |  |
| `serviceTasksLineItems[].workOrder.name` | string |  |
| `status` | string |  |
| `subTotal` | number |  |
| `summary` | string |  |
| `taxAmount` | number |  |
| `territory.id` | string |  |
| `territory.name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Zoho FSM API, this operation is `GET /Work_Orders/:recordId` (base URL `{{credentials.accessTokenRequest.api_domain}}/fsm/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-work-order.md) for the provider-specific parameters and requirements.

