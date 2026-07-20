# OnePlan: Get My Work Status Fields

Retrieves My Work status fields from OnePlan.

```
GET https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/get-my-work-status-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/get-my-work-status-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/get-my-work-status-fields?${params}`, {
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
      "AIEnabled": true,
      "AllowAdditions": true,
      "Choices": {},
      "ColumnAggregate": 1,
      "ColumnType": 1,
      "Decimals": 1,
      "DefaultValue": "string",
      "Description": "string",
      "DisplayName": "Ava Chen",
      "Function": 1,
      "Hidden": true,
      "Id": "string",
      "InternalName": "Ava Chen",
      "Locked": true,
      "MaxValue": 1,
      "MinValue": 1,
      "MultiLine": true,
      "Order": 1,
      "ParentFilterField": "string",
      "Percentage": true,
      "PlanTypeId": "string",
      "ReadOnly": true,
      "Required": true,
      "RollupAggregate": 1,
      "RollupWorkType": "string",
      "ShowInQuickStart": true,
      "System": true,
      "WriteablePlanTypes": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AIEnabled` | boolean |  |
| `AllowAdditions` | boolean |  |
| `Choices` | object |  |
| `ColumnAggregate` | number |  |
| `ColumnType` | number |  |
| `Decimals` | number |  |
| `DefaultValue` | string |  |
| `Description` | string |  |
| `DisplayName` | string |  |
| `Function` | number |  |
| `Hidden` | boolean |  |
| `Id` | string |  |
| `InternalName` | string |  |
| `Locked` | boolean |  |
| `MaxValue` | number |  |
| `MinValue` | number |  |
| `MultiLine` | boolean |  |
| `Order` | number |  |
| `ParentFilterField` | string |  |
| `Percentage` | boolean |  |
| `PlanTypeId` | string |  |
| `ReadOnly` | boolean |  |
| `Required` | boolean |  |
| `RollupAggregate` | number |  |
| `RollupWorkType` | string |  |
| `ShowInQuickStart` | boolean |  |
| `System` | boolean |  |
| `WriteablePlanTypes` | array<string> |  |

## Native endpoint

Through the native OnePlan API, this operation is `GET /mywork/statusfields` (base URL `https://my.oneplan.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-work-status-fields.md) for the provider-specific parameters and requirements.

