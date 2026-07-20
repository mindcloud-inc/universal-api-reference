# Viewpoint Spectrum: Get Customers



```
GET https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/get-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Spectrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/get-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/get-customers?${params}`, {
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
| `companyCode` | string | no |  |
| `pStatus` | list | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Address_1": "string",
      "Address_2": "string",
      "City": "string",
      "Company_Code": "string",
      "Customer_Code": "string",
      "Email1": "ava@example.com",
      "Error_Code": {},
      "Error_Column": {},
      "Error_Description": {},
      "First_Name": "Ava",
      "Last_Name": "Chen",
      "Name": "Ava Chen",
      "Phone_Number": {},
      "Price_Level_Material": {},
      "State": "string",
      "Status": "string",
      "Taxable_Flag": {},
      "Zip_Code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Address_1` | string |  |
| `Address_2` | string |  |
| `City` | string |  |
| `Company_Code` | string |  |
| `Customer_Code` | string |  |
| `Email1` | string |  |
| `Error_Code` | object |  |
| `Error_Column` | object |  |
| `Error_Description` | object |  |
| `First_Name` | string |  |
| `Last_Name` | string |  |
| `Name` | string |  |
| `Phone_Number` | object |  |
| `Price_Level_Material` | object |  |
| `State` | string |  |
| `Status` | string |  |
| `Taxable_Flag` | object |  |
| `Zip_Code` | string |  |

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `POST ws/GetCustomers` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customers.md) for the provider-specific parameters and requirements.

