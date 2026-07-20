# Zoho FSM: Create Estimate

Creates a new estimate in Zoho FSM.

```
POST https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho FSM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-estimate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[0].Company": "string",
  "data[0].Contact": "string",
  "data[0].serviceLineItems[].service": "string",
  "data[0].Summary": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-estimate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[0].Company": "string",
    "data[0].Contact": "string",
    "data[0].serviceLineItems[].service": "string",
    "data[0].Summary": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[0].adjustment` | number | no |  |
| `data[0].asset` | string | no |  |
| `data[0].billingAddress.id` | string | no |  |
| `data[0].Company` | string | yes |  |
| `data[0].Contact` | string | yes |  |
| `data[0].currency` | string | no |  |
| `data[0].email` | string | no |  |
| `data[0].exchangeRate` | number | no |  |
| `data[0].expiryDate` | date | no |  |
| `data[0].grandTotal` | number | no |  |
| `data[0].phone` | string | no |  |
| `data[0].serviceAddress.id` | string | no |  |
| `data[0].serviceLineItems[].amount` | number | no |  |
| `data[0].serviceLineItems[].contact` | string | no |  |
| `data[0].serviceLineItems[].description` | string | no |  |
| `data[0].serviceLineItems[].discount` | number | no |  |
| `data[0].serviceLineItems[].discountType` | string | no |  |
| `data[0].serviceLineItems[].lineItemAmount` | number | no |  |
| `data[0].serviceLineItems[].listPrice` | number | no |  |
| `data[0].serviceLineItems[].quantity` | number | no |  |
| `data[0].serviceLineItems[].sequence` | number | no |  |
| `data[0].serviceLineItems[].service` | string | yes |  |
| `data[0].serviceLineItems[].status` | string | no |  |
| `data[0].serviceLineItems[].tax.taxExemptionCode` | string | no |  |
| `data[0].serviceLineItems[].tax.taxExemptionId` | string | no |  |
| `data[0].serviceLineItems[].tax.taxId` | string | no |  |
| `data[0].serviceLineItems[].tax.taxName` | string | no |  |
| `data[0].serviceLineItems[].tax.taxPercentage` | number | no |  |
| `data[0].serviceLineItems[].unit` | string | no |  |
| `data[0].subTotal` | number | no |  |
| `data[0].Summary` | string | yes |  |
| `data[0].taxAmount` | number | no |  |
| `data[0].territory` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "data": {
        "Estimates": [
          {
            "Created_By": {
              "id": "string",
              "name": "Ava Chen"
            },
            "Created_Time": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "Modified_By": {
              "id": "string",
              "name": "Ava Chen"
            },
            "Modified_Time": "2026-05-07T12:00:00.000Z",
            "TabName": "Ava Chen",
            "UID": "string"
          }
        ],
        "Service_Line_Items": [
          {
            "Created_By": {
              "id": "string",
              "name": "Ava Chen"
            },
            "Created_Time": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "Modified_By": {
              "id": "string",
              "name": "Ava Chen"
            },
            "Modified_Time": "2026-05-07T12:00:00.000Z",
            "TabName": "Ava Chen",
            "UID": "string"
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
| `data.Estimates[].Created_By.id` | string |  |
| `data.Estimates[].Created_By.name` | string |  |
| `data.Estimates[].Created_Time` | date |  |
| `data.Estimates[].id` | string |  |
| `data.Estimates[].Modified_By.id` | string |  |
| `data.Estimates[].Modified_By.name` | string |  |
| `data.Estimates[].Modified_Time` | date |  |
| `data.Estimates[].TabName` | string |  |
| `data.Estimates[].UID` | string |  |
| `data.Service_Line_Items[].Created_By.id` | string |  |
| `data.Service_Line_Items[].Created_By.name` | string |  |
| `data.Service_Line_Items[].Created_Time` | date |  |
| `data.Service_Line_Items[].id` | string |  |
| `data.Service_Line_Items[].Modified_By.id` | string |  |
| `data.Service_Line_Items[].Modified_By.name` | string |  |
| `data.Service_Line_Items[].Modified_Time` | date |  |
| `data.Service_Line_Items[].TabName` | string |  |
| `data.Service_Line_Items[].UID` | string |  |
| `result` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho FSM API, this operation is `POST /Estimates` (base URL `{{credentials.accessTokenRequest.api_domain}}/fsm/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-estimate.md) for the provider-specific parameters and requirements.

