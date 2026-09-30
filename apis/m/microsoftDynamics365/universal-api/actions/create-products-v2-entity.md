# Microsoft Dynamics 365: Create ProductsV2 Entity



```
POST https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-products-v2-entity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-products-v2-entity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-products-v2-entity', {
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
| `AreIdenticalConfigurationsAllowed` | string | no |  |
| `EngChgProductOwnerId` | string | no |  |
| `HarmonizedSystemCode` | string | no |  |
| `IsAutomaticVariantGenerationEnabled` | string | no |  |
| `IsCatchWeightProduct` | string | no |  |
| `IsProductKit` | string | no | Yes/No |
| `IsProductVariantUnitConversionEnabled` | string | no | Yes/No |
| `NMFCCode` | string | no |  |
| `ProductColorGroupId` | string | no |  |
| `ProductDescription` | string | no |  |
| `ProductDimensionGroupName` | string | no |  |
| `ProductName` | string | no |  |
| `ProductSearchName` | string | no |  |
| `ProductSizeGroupId` | string | no |  |
| `ProductStyleGroupId` | string | no |  |
| `ProductSubType` | string | no |  |
| `ProductType` | string | no |  |
| `ProductVariantNameNomenclatureName` | string | no |  |
| `ProductVariantNumberNomenclatureName` | string | no |  |
| `RetailProductCategoryName` | string | no |  |
| `ServiceType` | string | no |  |
| `STCCCode` | string | no |  |
| `StorageDimensionGroupName` | string | no |  |
| `TrackingDimensionGroupName` | string | no |  |
| `VariantConfigurationTechnology` | string | no |  |
| `WarrantyDurationTime` | number | no |  |
| `WarrantyDurationTimeUnit` | string | no |  |
| `ProductNumber` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 API, this operation is `POST ProductsV2` (base URL `{{credentials.baseURL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-products-v2-entity.md) for the provider-specific parameters and requirements.

