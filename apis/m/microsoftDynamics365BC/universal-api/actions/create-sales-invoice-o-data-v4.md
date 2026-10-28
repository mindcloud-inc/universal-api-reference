# Microsoft Dynamics 365 BC: Create Sales Invoice ODataV4



```
POST https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-sales-invoice-o-data-v4
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 BC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-sales-invoice-o-data-v4" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-sales-invoice-o-data-v4', {
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
| `company` | list | no |  |
| `No` | string | no |  |
| `Posting_Date` | string | no |  |
| `Due_Date` | string | no |  |
| `Bill_to_Name` | string | no |  |
| `Sell_to_City` | string | no |  |
| `Sell_to_Country_Region_Code` | string | no |  |
| `Sell_to_County` | string | no |  |
| `Sell_to_Post_Code` | string | no |  |
| `Bill_to_Address` | string | no |  |
| `Bill_to_Address_2` | string | no |  |
| `Bill_to_City` | string | no |  |
| `Bill_to_Country_Region_Code` | string | no |  |
| `Bill_to_County` | string | no |  |
| `Bill_to_Post_Code` | string | no |  |
| `Ship_to_Address` | string | no |  |
| `Ship_to_Address_2` | string | no |  |
| `Ship_to_City` | string | no |  |
| `Ship_to_Country_Region_Code` | string | no |  |
| `Ship_to_County` | string | no |  |
| `Ship_to_Post_Code` | string | no |  |
| `Salesperson_Code` | string | no |  |
| `Sell_to_Customer_No` | string | no |  |
| `Sell_to_Customer_Name` | string | no |  |
| `Posting_Description` | string | no |  |
| `Sell_to_Contact` | string | no |  |
| `Your_Reference` | string | no |  |
| `Document_Date` | string | no |  |
| `Assigned_User_ID` | string | no |  |
| `Shipment_Date` | string | no |  |
| `Prices_Including_VAT` | boolean | no |  |
| `VAT_Country_Region_Code` | string | no |  |
| `Payment_Terms_Code` | string | no |  |
| `Tax_Liable` | boolean | no |  |
| `Tax_Area_Code` | string | no |  |
| `Shortcut_Dimension_1_Code` | string | no |  |
| `ShippingOptions` | string | no |  |
| `Bill_to_Contact` | string | no |  |
| `Class_Code` | string | no |  |
| `External_Document_No` | string | no |  |
| `Shortcut_Dimension_2_Code` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 BC API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 BC API, this operation is `POST https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/MindcloudSalesInvoice` (base URL `https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sales-invoice-o-data-v4.md) for the provider-specific parameters and requirements.

