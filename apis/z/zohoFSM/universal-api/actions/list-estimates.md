# Zoho FSM: List Estimates

Retrieves estimates from Zoho FSM.

```
GET https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-estimates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho FSM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-estimates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-estimates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "$editable": true,
      "$inactive": true,
      "$permissions": {
        "delete": true,
        "edit": true,
        "read": true
      },
      "Adjustment": 1,
      "Billing_Address": {
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
      "Service_Address": {
        "id": "string",
        "name": "Ava Chen",
        "Service_City": "string",
        "Service_Country": "string",
        "Service_State": "string",
        "Service_Street_1": "string",
        "Service_Zip_Code": "string"
      },
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
| `$editable` | boolean |  |
| `$inactive` | boolean |  |
| `$permissions.delete` | boolean |  |
| `$permissions.edit` | boolean |  |
| `$permissions.read` | boolean |  |
| `Adjustment` | number |  |
| `Billing_Address.Billing_City` | string |  |
| `Billing_Address.Billing_Country` | string |  |
| `Billing_Address.Billing_State` | string |  |
| `Billing_Address.Billing_Street_1` | string |  |
| `Billing_Address.Billing_Zip_Code` | string |  |
| `Billing_Address.id` | string |  |
| `Billing_Address.name` | string |  |
| `Company.id` | string |  |
| `Company.name` | string |  |
| `Contact.id` | string |  |
| `Contact.name` | string |  |
| `Created_By.email` | string |  |
| `Created_By.id` | string |  |
| `Created_By.name` | string |  |
| `Created_Time` | date |  |
| `Currency` | string |  |
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
| `Service_Address.id` | string |  |
| `Service_Address.name` | string |  |
| `Service_Address.Service_City` | string |  |
| `Service_Address.Service_Country` | string |  |
| `Service_Address.Service_State` | string |  |
| `Service_Address.Service_Street_1` | string |  |
| `Service_Address.Service_Zip_Code` | string |  |
| `Status` | string |  |
| `Sub_Total` | number |  |
| `Summary` | string |  |
| `Tax_Amount` | number |  |
| `Territory.id` | string |  |
| `Territory.name` | string |  |

## Native endpoint

Through the native Zoho FSM API, this operation is `GET /Estimates` (base URL `{{credentials.accessTokenRequest.api_domain}}/fsm/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-estimates.md) for the provider-specific parameters and requirements.

