# Wodely: Create Task Packages in Batch



```
POST https://connect.mindcloud.co/v1/universal/wodely/latest/actions/create-task-packages-in-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wodely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wodely/latest/actions/create-task-packages-in-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskGuid": "your-task-guid",
  "packages[].productDesc": "Verification package"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wodely/latest/actions/create-task-packages-in-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskGuid": "your-task-guid",
    "packages[].productDesc": "Verification package"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskGuid` | string | yes | Task identifier returned by Wodely. Example: `your-task-guid`. |
| `packages[].productId` | string | no | Product Id or item Id |
| `packages[].productDesc` | string | yes | Short description of the package item. Example: `Verification package`. |
| `packages[].orderId` | string | no | Order Id |
| `packages[].quantity` | number | no | Quantity for each package line. Example: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deleteOldPackages` | boolean | no | Delete all existing packages on the task before adding the new ones. |
| `packages[].weight` | number | no | Weight for each package line. Example: `2.5`. |
| `packages[].price` | number | no | Price or line total for each package line. Example: `19.99`. |
| `packages[].packageTypeId` | number | no | Package type identifier. Example: `10`. |
| `packages[].labelId` | string | no | Label or barcode |
| `packages[].field1` | string | no | Custom Field 1 |
| `packages[].field2` | string | no | Custom Field 2 |
| `packages[].field3` | string | no | Custom Field 3 |
| `packages[].field4` | string | no | Custom Field 4 |
| `packages[].field5` | string | no | Custom Field 5 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field1": "string",
      "field2": "string",
      "field3": "string",
      "field4": "string",
      "field5": "string",
      "id": 1,
      "labelId": "string",
      "orderId": "string",
      "packageTypeDesc": "string",
      "packageTypeId": 1,
      "price": 1,
      "productDesc": "string",
      "productId": "string",
      "quantity": 1,
      "taskId": 1,
      "weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field1` | string | Custom field 1. |
| `field2` | string | Custom field 2. |
| `field3` | string | Custom field 3. |
| `field4` | string | Custom field 4. |
| `field5` | string | Custom field 5. |
| `id` | number | Package identifier. |
| `labelId` | string | Package label or barcode identifier. |
| `orderId` | string | Order identifier associated with the package. |
| `packageTypeDesc` | string | Package type description. |
| `packageTypeId` | number | Package type identifier. |
| `price` | number | Package price or line total. |
| `productDesc` | string | Package product description. |
| `productId` | string | Product or item identifier. |
| `quantity` | number | Package quantity. |
| `taskId` | number | Numeric task identifier linked to the package. |
| `weight` | number | Package weight. |

## Native endpoint

Through the native Wodely API, this operation is `POST /v2/taskPackages` (base URL `https://api.wodely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task-packages-in-batch.md) for the provider-specific parameters and requirements.

