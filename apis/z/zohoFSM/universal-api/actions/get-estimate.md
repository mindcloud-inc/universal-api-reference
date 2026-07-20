# Zoho FSM: Get Estimate

Retrieves estimate details from Zoho FSM.

```
GET https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/get-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho FSM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/get-estimate?connectionId=$CONNECTION_ID&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/get-estimate?${params}`, {
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
      "Adjustment": 1,
      "Billing_Address": {
        "Billing_Address_Name": "Ava Chen",
        "Billing_City": "string",
        "Billing_Country": "string",
        "Billing_State": "string",
        "Billing_Street_1": "string",
        "Billing_Zip_Code": "string",
        "id": "string",
        "name": "Ava Chen"
      },
      "Company": {
        "id": "string",
        "name": "Ava Chen"
      },
      "Config": "string",
      "Contact": {
        "id": "string",
        "name": "Ava Chen"
      },
      "Created_By": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "Created_Time": "2026-05-07T12:00:00.000Z",
      "Currency": "string",
      "Discount_Type": "string",
      "Email": "ava@example.com",
      "Exchange_Rate": 1,
      "Expiry_Date": "2026-05-07T12:00:00.000Z",
      "Grand_Total": 1,
      "id": "string",
      "Modified_By": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "Modified_Time": "2026-05-07T12:00:00.000Z",
      "Name": "Ava Chen",
      "Owner": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "Phone": "string",
      "Round_Off": 1,
      "Service_Address": {
        "id": "string",
        "name": "Ava Chen",
        "Service_Address_Name": "Ava Chen",
        "Service_City": "string",
        "Service_Country": "string",
        "Service_State": "string",
        "Service_Street_1": "string",
        "Service_Zip_Code": "string"
      },
      "Service_Line_Items": [
        {
          "Amount": 1,
          "Billing_Status": "string",
          "Contact": {
            "id": "string",
            "name": "Ava Chen"
          },
          "Created_By": {
            "email": "ava@example.com",
            "id": "string",
            "name": "Ava Chen"
          },
          "Created_Time": "2026-05-07T12:00:00.000Z",
          "Currency": "string",
          "Customer_Preference": 1,
          "Discount": 1,
          "Discount_Type": "string",
          "Estimate": {
            "id": "string",
            "name": "Ava Chen"
          },
          "Exchange_Rate": 1,
          "id": "string",
          "Is_Optional": true,
          "Line_Item_Amount": 1,
          "List_Price": 1,
          "Modified_By": {
            "email": "ava@example.com",
            "id": "string",
            "name": "Ava Chen"
          },
          "Modified_Time": "2026-05-07T12:00:00.000Z",
          "Name": "Ava Chen",
          "Owner": {
            "email": "ava@example.com",
            "id": "string",
            "name": "Ava Chen"
          },
          "Quantity": 1,
          "Quantity_Source": "string",
          "Sequence": 1,
          "Service": {
            "id": "string",
            "name": "Ava Chen"
          },
          "Status": "string",
          "Unit": "string",
          "User_Preference": true
        }
      ],
      "Status": "string",
      "Sub_Total": 1,
      "Summary": "string",
      "Tax_Amount": 1,
      "Territory": {
        "id": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Adjustment` | number |  |
| `Billing_Address.Billing_Address_Name` | string |  |
| `Billing_Address.Billing_City` | string |  |
| `Billing_Address.Billing_Country` | string |  |
| `Billing_Address.Billing_State` | string |  |
| `Billing_Address.Billing_Street_1` | string |  |
| `Billing_Address.Billing_Zip_Code` | string |  |
| `Billing_Address.id` | string |  |
| `Billing_Address.name` | string |  |
| `Company.id` | string |  |
| `Company.name` | string |  |
| `Config` | string |  |
| `Contact.id` | string |  |
| `Contact.name` | string |  |
| `Created_By.email` | string |  |
| `Created_By.id` | string |  |
| `Created_By.name` | string |  |
| `Created_Time` | date |  |
| `Currency` | string |  |
| `Discount_Type` | string |  |
| `Email` | string |  |
| `Exchange_Rate` | number |  |
| `Expiry_Date` | date |  |
| `Grand_Total` | number |  |
| `id` | string |  |
| `Modified_By.email` | string |  |
| `Modified_By.id` | string |  |
| `Modified_By.name` | string |  |
| `Modified_Time` | date |  |
| `Name` | string |  |
| `Owner.email` | string |  |
| `Owner.id` | string |  |
| `Owner.name` | string |  |
| `Phone` | string |  |
| `Round_Off` | number |  |
| `Service_Address.id` | string |  |
| `Service_Address.name` | string |  |
| `Service_Address.Service_Address_Name` | string |  |
| `Service_Address.Service_City` | string |  |
| `Service_Address.Service_Country` | string |  |
| `Service_Address.Service_State` | string |  |
| `Service_Address.Service_Street_1` | string |  |
| `Service_Address.Service_Zip_Code` | string |  |
| `Service_Line_Items[].Amount` | number |  |
| `Service_Line_Items[].Billing_Status` | string |  |
| `Service_Line_Items[].Contact.id` | string |  |
| `Service_Line_Items[].Contact.name` | string |  |
| `Service_Line_Items[].Created_By.email` | string |  |
| `Service_Line_Items[].Created_By.id` | string |  |
| `Service_Line_Items[].Created_By.name` | string |  |
| `Service_Line_Items[].Created_Time` | date |  |
| `Service_Line_Items[].Currency` | string |  |
| `Service_Line_Items[].Customer_Preference` | number |  |
| `Service_Line_Items[].Discount` | number |  |
| `Service_Line_Items[].Discount_Type` | string |  |
| `Service_Line_Items[].Estimate.id` | string |  |
| `Service_Line_Items[].Estimate.name` | string |  |
| `Service_Line_Items[].Exchange_Rate` | number |  |
| `Service_Line_Items[].id` | string |  |
| `Service_Line_Items[].Is_Optional` | boolean |  |
| `Service_Line_Items[].Line_Item_Amount` | number |  |
| `Service_Line_Items[].List_Price` | number |  |
| `Service_Line_Items[].Modified_By.email` | string |  |
| `Service_Line_Items[].Modified_By.id` | string |  |
| `Service_Line_Items[].Modified_By.name` | string |  |
| `Service_Line_Items[].Modified_Time` | date |  |
| `Service_Line_Items[].Name` | string |  |
| `Service_Line_Items[].Owner.email` | string |  |
| `Service_Line_Items[].Owner.id` | string |  |
| `Service_Line_Items[].Owner.name` | string |  |
| `Service_Line_Items[].Quantity` | number |  |
| `Service_Line_Items[].Quantity_Source` | string |  |
| `Service_Line_Items[].Sequence` | number |  |
| `Service_Line_Items[].Service.id` | string |  |
| `Service_Line_Items[].Service.name` | string |  |
| `Service_Line_Items[].Status` | string |  |
| `Service_Line_Items[].Unit` | string |  |
| `Service_Line_Items[].User_Preference` | boolean |  |
| `Status` | string |  |
| `Sub_Total` | number |  |
| `Summary` | string |  |
| `Tax_Amount` | number |  |
| `Territory.id` | string |  |
| `Territory.name` | string |  |

## Native endpoint

Through the native Zoho FSM API, this operation is `GET /Estimates/:recordId` (base URL `{{credentials.accessTokenRequest.api_domain}}/fsm/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-estimate.md) for the provider-specific parameters and requirements.

