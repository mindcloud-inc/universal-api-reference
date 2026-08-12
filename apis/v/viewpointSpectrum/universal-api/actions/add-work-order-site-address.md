# Viewpoint Spectrum: Add Work Order Site Address



```
POST https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/add-work-order-site-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Spectrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/add-work-order-site-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/add-work-order-site-address', {
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
| `Site_ID` | string | no |  |
| `Site_Name` | string | no |  |
| `Site_Address1` | string | no |  |
| `Site_Address2` | string | no |  |
| `Site_City` | string | no |  |
| `Site_State` | string | no |  |
| `Site_Zip_Code` | string | no |  |
| `Site_Phone1` | string | no |  |
| `Site_Phone2` | string | no |  |
| `Telephone_Ext_1` | string | no |  |
| `Telephone_Ext_2` | string | no |  |
| `Site_Contact_Person` | string | no |  |
| `Site_Customer_Code` | string | no |  |
| `Lead_Source` | string | no |  |
| `Requested_Tech` | string | no |  |
| `WO_Type` | string | no |  |
| `Zone` | string | no |  |
| `Special_Instructions` | string | no |  |
| `Show_Notes` | string | no |  |
| `Sales_Tax_Code` | string | no |  |
| `Taxable_Flag` | string | no |  |
| `Labor_Taxable` | string | no |  |
| `Material_Taxable` | string | no |  |
| `Work_Comp_Code` | string | no |  |
| `Wage_Rate_Level` | string | no |  |
| `Work_State_Tax_Code` | string | no |  |
| `Work_County_Tax_Code` | string | no |  |
| `Work_Local_Tax_Code` | string | no |  |
| `Work_Site_Email` | string | no |  |
| `Site_Case_Type` | string | no |  |
| `Customer_Job` | string | no |  |
| `Latitude` | string | no |  |
| `Longitude` | string | no |  |
| `Markup_Code` | string | no |  |
| `Alternate_Address` | string | no |  |
| `Billto_Code` | string | no |  |
| `Cost_Center` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Spectrum API returns.

## Native endpoint

Through the native Viewpoint Spectrum API, this operation is `POST ws/AddWOSiteAddress` (base URL `{{credentials.url}}:8482/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-work-order-site-address.md) for the provider-specific parameters and requirements.

