# Microsoft Dynamics 365 BC: Get Item



```
GET https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 BC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/get-item?connectionId=$CONNECTION_ID&companyId=string&itemId=fca5738a-44e3-ea11-bb43-000d3a2feca1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string",
  "itemId": "fca5738a-44e3-ea11-bb43-000d3a2feca1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/get-item?${params}`, {
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
| `companyId` | list<string> | yes | The Business Central company that holds the item. |
| `itemId` | string | yes | The item's system ID (GUID), not the item number. Example: `fca5738a-44e3-ea11-bb43-000d3a2feca1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseUnitOfMeasureCode": "string",
      "baseUnitOfMeasureId": "string",
      "blocked": true,
      "displayName": "Ava Chen",
      "displayName2": "Ava Chen",
      "generalProductPostingGroupCode": "string",
      "generalProductPostingGroupId": "string",
      "gtin": "string",
      "id": "string",
      "inventory": 1,
      "inventoryPostingGroupCode": "string",
      "inventoryPostingGroupId": "string",
      "itemCategoryCode": "string",
      "itemCategoryId": "string",
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "number": "string",
      "priceIncludesTax": true,
      "taxGroupCode": "string",
      "taxGroupId": "string",
      "type": "string",
      "unitCost": 1,
      "unitPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseUnitOfMeasureCode` | string |  |
| `baseUnitOfMeasureId` | string |  |
| `blocked` | boolean |  |
| `displayName` | string |  |
| `displayName2` | string |  |
| `generalProductPostingGroupCode` | string |  |
| `generalProductPostingGroupId` | string |  |
| `gtin` | string |  |
| `id` | string |  |
| `inventory` | number |  |
| `inventoryPostingGroupCode` | string |  |
| `inventoryPostingGroupId` | string |  |
| `itemCategoryCode` | string |  |
| `itemCategoryId` | string |  |
| `lastModifiedDateTime` | date |  |
| `number` | string |  |
| `priceIncludesTax` | boolean |  |
| `taxGroupCode` | string |  |
| `taxGroupId` | string |  |
| `type` | string |  |
| `unitCost` | number |  |
| `unitPrice` | number |  |

## Native endpoint

Through the native Microsoft Dynamics 365 BC API, this operation is `GET v2.0/companies(:companyId)/items(:itemId)` (base URL `https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

