# Microsoft Dynamics 365 BC: Create Credit Memo Itens ODataV4



```
GET https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-credit-memo-itens-o-data-v4
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 BC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-credit-memo-itens-o-data-v4?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/create-credit-memo-itens-o-data-v4?${params}`, {
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
| `company` | list | no |  |
| `Type` | string | no |  |
| `No` | string | no |  |
| `Item_Reference_No` | string | no |  |
| `Description` | string | no |  |
| `Quantity` | number | no |  |
| `Unit_Price` | number | no |  |
| `Tax_Area_Code` | string | no |  |
| `Line_Amount` | number | no |  |
| `Allow_Invoice_Disc` | boolean | no |  |
| `Shortcut_Dimension_1_Code` | string | no |  |
| `Work_Type_Code` | string | no |  |
| `Document_No` | string | no |  |
| `Description_2` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 BC API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 BC API, this operation is `POST https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/ODataV4/Company(:company)/MindcloudCreditMemoSalesLines` (base URL `https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/create-credit-memo-itens-o-data-v4.md) for the provider-specific parameters and requirements.

