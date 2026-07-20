# Zoho FSM: Get Company

Retrieves company details from Zoho FSM.

```
GET https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho FSM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/get-company?connectionId=$CONNECTION_ID&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/get-company?${params}`, {
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
      "$currency_symbol": "string",
      "$editable": true,
      "$inactive": true,
      "$permissions": {
        "delete": true,
        "edit": true,
        "read": true
      },
      "Billing_Address": {
        "Address_Name": "Ava Chen",
        "City": "string",
        "Country": "string",
        "id": "string",
        "name": "Ava Chen",
        "State": "string",
        "Street_1": "string",
        "Street_2": "string",
        "Zip_Code": "string"
      },
      "Company_Name": "Ava Chen",
      "Company_Type": "string",
      "Config": "string",
      "Created_By": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "Created_Time": "2026-05-07T12:00:00.000Z",
      "Currency": "string",
      "Email": "ava@example.com",
      "Exchange_Rate": 1,
      "Fax": "string",
      "id": "string",
      "Modified_By": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "Modified_Time": "2026-05-07T12:00:00.000Z",
      "Owner": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "Phone": "string",
      "Service_Address": {
        "Address_Name": "Ava Chen",
        "City": "string",
        "Country": "string",
        "id": "string",
        "name": "Ava Chen",
        "State": "string",
        "Street_1": "string",
        "Street_2": "string",
        "Zip_Code": "string"
      },
      "Tax": {
        "Taxable": true
      },
      "Website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$currency_symbol` | string |  |
| `$editable` | boolean |  |
| `$inactive` | boolean |  |
| `$permissions.delete` | boolean |  |
| `$permissions.edit` | boolean |  |
| `$permissions.read` | boolean |  |
| `Billing_Address.Address_Name` | string |  |
| `Billing_Address.City` | string |  |
| `Billing_Address.Country` | string |  |
| `Billing_Address.id` | string |  |
| `Billing_Address.name` | string |  |
| `Billing_Address.State` | string |  |
| `Billing_Address.Street_1` | string |  |
| `Billing_Address.Street_2` | string |  |
| `Billing_Address.Zip_Code` | string |  |
| `Company_Name` | string |  |
| `Company_Type` | string |  |
| `Config` | string |  |
| `Created_By.email` | string |  |
| `Created_By.id` | string |  |
| `Created_By.name` | string |  |
| `Created_Time` | date |  |
| `Currency` | string |  |
| `Email` | string |  |
| `Exchange_Rate` | number |  |
| `Fax` | string |  |
| `id` | string |  |
| `Modified_By.email` | string |  |
| `Modified_By.id` | string |  |
| `Modified_By.name` | string |  |
| `Modified_Time` | date |  |
| `Owner.email` | string |  |
| `Owner.id` | string |  |
| `Owner.name` | string |  |
| `Phone` | string |  |
| `Service_Address.Address_Name` | string |  |
| `Service_Address.City` | string |  |
| `Service_Address.Country` | string |  |
| `Service_Address.id` | string |  |
| `Service_Address.name` | string |  |
| `Service_Address.State` | string |  |
| `Service_Address.Street_1` | string |  |
| `Service_Address.Street_2` | string |  |
| `Service_Address.Zip_Code` | string |  |
| `Tax.Taxable` | boolean |  |
| `Website` | string |  |

## Native endpoint

Through the native Zoho FSM API, this operation is `GET /Companies/:recordId` (base URL `{{credentials.accessTokenRequest.api_domain}}/fsm/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

