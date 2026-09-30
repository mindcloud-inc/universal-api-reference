# Microsoft Dynamics 365: Create Project Sales Item Requirement



```
POST https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-project-sales-item-requirement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-project-sales-item-requirement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-project-sales-item-requirement', {
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
| `ActivityNumber` | string | no |  |
| `CurrencyCode` | string | no |  |
| `ItemId` | string | no |  |
| `ProjectCategoryId` | string | no |  |
| `ProjectId` | string | no |  |
| `ProjectLinePropertyId` | string | no |  |
| `ReceiptDateConfirmed` | string | no |  |
| `ReceiptDateRequested` | string | no |  |
| `SalesPrice` | number | no |  |
| `SalesQuantity` | number | no |  |
| `SalesUnit` | string | no |  |
| `ShipDate` | string | no |  |
| `ShippingDateConfirmed` | string | no |  |
| `ShippingDateRequested` | string | no |  |
| `ShippingSiteId` | string | no |  |
| `ShippingWarehouseId` | string | no |  |
| `TCIEstNotes` | string | no |  |
| `TCIRoomQty` | number | no |  |
| `dataAreaId` | string | no |  |
| `TCIOwnerFurnished` | string | no | Yes / No |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 API, this operation is `POST ProjectSalesItemRequirements` (base URL `{{credentials.baseURL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-sales-item-requirement.md) for the provider-specific parameters and requirements.

